# Workshop 4 — Dependency Map + Critical Path

## Sản phẩm: AI Career Advisor Assistant (A20)

> "Mỗi Tier 1 dependency phải có Plan B sẵn sàng deploy trong 24 giờ."

---

## 3 External Dependencies

### 🔴 Dependency 1: OpenRouter / LLM API (Tier 1 — Critical)

**Worst-case:** OpenRouter siết rate limit hoặc tăng giá 5x đột ngột. Free models bị remove. Sản phẩm phụ thuộc 100% vào LLM để trả lời chatbot — API down = product down.

**Plan B:**
- Code **abstraction layer** cho LLM client (`ml/llm_client.py` đã có wrapper). Switch sang **Google Gemini API** (có free tier) hoặc **Anthropic Claude** trong 24h.
- **Caching layer** cho top 50 câu hỏi thường gặp (Redis — `infrastructure/cache/redis.py` đã có skeleton). Phục vụ 60–70% queries mà không cần LLM call.
- Fallback cuối: **local model** (Ollama + Llama 3) cho basic queries. Latency cao hơn nhưng vẫn hoạt động.

**Cost:** 1 tuần dev tích hợp Gemini/Claude fallback. Redis caching: 2 ngày. Local model setup: 3 ngày. **Tổng: ~2 tuần.** Chưa build hoàn chỉnh — cần implement trước khi go live.

---

### 🔴 Dependency 2: MongoDB Atlas + Qdrant Cloud (Tier 1 — Critical)

**Worst-case:** MongoDB Atlas outage hoặc free tier hết quota. Qdrant cloud instance bị xóa. Toàn bộ data pipeline (Bronze → Silver → Gold) và hybrid search (vector + keyword) ngừng hoạt động. Backend trả 500 error cho mọi request.

**Plan B:**
- `InMemoryJobRepository` fallback **đã có code** trong backend (`infrastructure/db/` — ghi chú từ JOURNAL tuần 6). Khi MongoDB unavailable, tự động switch sang 12 in-memory job fixtures.
- Backup: export MongoDB data hàng ngày ra JSON files (Bronze format). Nếu cần, import lại vào **PostgreSQL + pgvector** (alternative stack) trong 3–5 ngày.
- Qdrant fallback: **FAISS local** (`infrastructure/vector_db/faiss.py` đã có skeleton). Chất lượng search giảm nhẹ nhưng vẫn hoạt động.

**Cost:** InMemoryRepository: 0 ngày (đã có). Daily backup script: 1 ngày. PostgreSQL migration: 5 ngày nếu cần. **Plan B sẵn sàng cho fallback ngay lập tức** (in-memory).

---

### 🟡 Dependency 3: Nền tảng tuyển dụng (TopCV, LinkedIn, Indeed) — Data Source (Tier 2 — Important)

**Worst-case:** TopCV block IP crawl hoặc đổi HTML structure. LinkedIn siết rate limit API. Indeed thêm CAPTCHA. Không crawl được JD mới → data cũ → insight lỗi thời → user mất tin tưởng.

**Plan B:**
- **Multi-source strategy** (đã implement — ADR-13): Không phụ thuộc 1 nguồn. Nếu TopCV block → vẫn có LinkedIn, Indeed, ITviec, VietnamWorks.
- **Public datasets** fallback: Kaggle TopCV 2026, GitHub job crawlers community. Không real-time nhưng có data baseline.
- **RSS/API public** (ADR-10): ITviec có RSS feed, một số nền tảng có public API. 100% legal.
- **User-submitted JD** (ADR-10): User paste JD vào app → AI analyze. Zero crawl risk, 100% legal.
- **Polite crawling** (rate limit 1 req/min, robots.txt compliance) giảm rủi ro bị block.

**Cost:** Switch sang backup source: 2–3 ngày per source. Public dataset integration: 1 tuần. User-submitted flow: 3 ngày (backend endpoint `/cv/upload` đã có skeleton). **Tổng: deployable trong 7 ngày.**

---

### Cascading Failure Analysis

> **Nếu Dependency 1 (LLM) + Dependency 2 (DB) fail cùng lúc:**

- Chatbot Agent: **DOWN** (không có LLM + không có data)
- Dashboard: **DOWN** (không có DB)
- Export PDF: **DOWN** (không có data)
- **Mitigation:** InMemoryRepository (12 fixtures) + Redis cache (top 50 queries) → Chatbot trả lời được ~30% câu hỏi cơ bản. Dashboard hiển thị cached data. **Không ideal nhưng không chết hoàn toàn.**
- **Single point of failure:** Supabase Auth. Nếu Supabase down → user không login được → 100% down. Cần thêm **email/password fallback** hoặc **guest mode** cho emergency.

---

## Critical Path

```
JD Crawl Pipeline ──→ Data Normalize ──→ MongoDB Import ──→ API Integration ──→ Launch
   (multi-source)      (Bronze→Silver     (Silver→Gold       (Frontend ↔
    ADR-10, ADR-13      →Gold)             + Qdrant index)    Backend)
        │                   │                   │                  │
        ▼                   ▼                   ▼                  ▼
   Legal Compliance    Schema Unify        Hybrid Search      End-to-end
   (robots.txt,        (TopCV ≠ LinkedIn   (Vector 0.7 +      testing
    rate limit,         ≠ Indeed format)    Keyword 0.3)
    ADR-10)
```

### Critical Path (chuỗi dài nhất — trễ 1 ngày = trễ launch 1 ngày):

```
Legal Compliance → JD Crawl Pipeline → Data Normalize → MongoDB Import → API Integration → Launch
```

**6 task tuần tự. Không thể parallel.** Đây là critical path vì:
- Không clear legal → không dám crawl
- Không crawl → không có data
- Không normalize → không import được vào MongoDB
- Không có data trong DB → API trả empty
- API empty → Frontend vô nghĩa

### Non-critical (có buffer, parallel được):

| Task | Parallel với | Buffer |
|---|---|---|
| UI Polish (responsive, dark mode) | MongoDB Import, API Integration | Cao — làm bất kỳ lúc nào |
| i18n refinement | Mọi critical task | Cao — đã hoạt động, chỉ polish |
| Export PDF polish | API Integration | Trung bình — cần real data nhưng mock đã hoạt động |
| Documentation + README | Mọi task | Cao — independent |
| Deployment setup (Railway) | Data Normalize, MongoDB Import | Thấp — cần chạy thử với data thật |

---

## Tóm tắt

| Dependency | Tier | Plan B sẵn? | Deploy trong |
|---|---|---|---|
| OpenRouter/LLM API | 🔴 Tier 1 | Partial (abstraction layer có, caching chưa) | 2 tuần |
| MongoDB + Qdrant | 🔴 Tier 1 | Ready (InMemoryRepo đã có code) | 0 ngày fallback, 5 ngày full migration |
| Nền tảng tuyển dụng | 🟡 Tier 2 | Ready (multi-source + public dataset) | 7 ngày |

> **Ưu tiên #1:** Build caching layer cho LLM queries — đây là Plan B yếu nhất hiện tại.
>
> **Critical Path:** Legal → Crawl → Normalize → Import → API → Launch. **Focus toàn bộ engineering effort vào chuỗi này.**
