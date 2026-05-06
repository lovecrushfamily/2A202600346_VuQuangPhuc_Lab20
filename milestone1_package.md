# Milestone 1 — Investor Package

## AI Career Advisor Assistant

> **Seed Round Package — Day 16–20**

---

<!-- TRANG 1: COVER + EXECUTIVE SUMMARY -->

## Trang 1 — Cover & Executive Summary

### AI Career Advisor Assistant

**Team A20** — Vũ Quang Phúc · Vũ Văn Huân · Nguyễn Công Thành

---

#### Twitter Pitch (280 ký tự)

> AI Career Advisor Assistant giúp **career advisors và HR tại VN** giảm **5+ giờ/tuần** nghiên cứu thị trường lao động bằng chatbot agent trả lời kèm trích dẫn nguồn từ **4.000+ JD aggregate**. Pilot 3 trường ĐH. LTV/CAC = 3.2x, payback 8 tháng. Gọi **500M VND seed** để đạt 200 tổ chức trong 12 tháng.

---

#### Executive Summary

Career advisors, HR và recruiters tại Việt Nam mất hàng tuần mỗi tháng tổng hợp thủ công thị trường tuyển dụng từ nhiều nền tảng rời rạc. Hiện không có công cụ nào tự động aggregate insight từ JD thật với trích dẫn nguồn.

**AI Career Advisor Assistant** tự động hoá pipeline: crawl JD → normalize → aggregate → insight — cho phép tra cứu thị trường bằng ngôn ngữ tự nhiên, xem dashboard KPI, và export báo cáo PDF. Mỗi con số kèm nền tảng nguồn và thời điểm tổng hợp.

**Đang gọi 500M VND seed** để hoàn thiện data pipeline, đạt 200 tổ chức sử dụng, và validate PMF trong 12 tháng.

---

<!-- TRANG 2: PITCH MEMO -->

## Trang 2 — Pitch Memo (1-pager, Day 19)

### 1. THE PROBLEM

Career advisors tại các trường ĐH và trung tâm tuyển dụng mất **5–8 giờ/tuần** tổng hợp thủ công thị trường lao động từ TopCV, VietnamWorks, LinkedIn, ITviec. Mỗi tuần data cũ, insight lệch hướng, tư vấn thiếu căn cứ.

### 2. THE INSIGHT

Các nền tảng tuyển dụng **chỉ phục vụ job seeker** (matching CV → JD). Không ai phục vụ **career advisor** — người cần nhìn toàn cảnh thị trường để tư vấn cho hàng trăm sinh viên. Insight aggregate có nguồn trích dẫn là khoảng trống chưa ai lấp.

### 3. THE SOLUTION

- **Chatbot Agent** trả lời bằng ngôn ngữ tự nhiên, kèm **trích dẫn nguồn JD gốc** (link, platform badge) — không hiển thị raw JD (tuân thủ ADR-10).
- **Differentiator vs ChatGPT:** ChatGPT trả lời generic, không có data thị trường VN real-time. Chúng tôi có pipeline crawl JD thật từ 5 nền tảng, aggregate insight có nguồn.
- **AI giúp:** Hybrid Search (0.7 Vector + 0.3 Keyword) + Reranker cho kết quả chính xác. Agent reasoning giải thích "vì sao" — không chỉ trả số.

### 4. WHY NOW

- Chi phí LLM API giảm 10x trong 2 năm (GPT-4 → GPT-4o-mini) — lần đầu tiên AI aggregate insight khả thi cho startup early-stage.
- Thị trường tuyển dụng VN đang số hoá nhanh — TopCV, ITviec đều có cấu trúc dữ liệu parse được.
- Career advisors tại ĐH đang bị áp lực lớn tư vấn đúng hướng khi ngành thay đổi nhanh hơn giáo trình.

### 5. TRACTION / PROOF

- **4.000+ JD links** đã crawl từ TopCV, LinkedIn, Indeed (multi-source pipeline hoạt động).
- **MVP chạy được:** Frontend React/Vite + Supabase Auth + Edge Function chatbot. Dashboard 6 KPIs + line chart + Export PDF.
- **Backend production-ready:** FastAPI 16-phase architecture, Hybrid Search, Matching Pipeline (4/4 test cases pass), Medallion Data Pipeline (Bronze → Silver → Gold).
- **5 sprint hoàn thành** trong 5 tuần — team 3 người ship liên tục.

### 6. THE ASK

Gọi **500M VND seed** để:
- Hoàn thiện data pipeline real-time (scheduled crawl + aggregate)
- Đạt **50 career advisors pilot** dùng ≥ 3 lần/tuần trong 6 tháng đầu
- Mở rộng lên **200 tổ chức** (ĐH, trung tâm tuyển dụng, phòng HR) trong 12 tháng

---

<!-- TRANG 3: MARKET ANALYSIS -->

## Trang 3 — Market Analysis (Day 16)

### TAM / SAM / SOM

| Layer | Estimate | Key Assumptions | Confidence |
|---|---|---|---|
| **TAM** | 800B – 1.200B VND/năm | ~50.000 career advisors + HR managers tại VN × 200K–300K VND/tháng subscription. Nguồn: GSO 2025 (28.000 cơ sở giáo dục + 15.000 công ty tuyển dụng thường xuyên) | Low |
| **SAM** | 120B – 200B VND/năm | ~5.000 career advisors tại ĐH + trung tâm tuyển dụng lớn × 200K VND/tháng. Segment có nhu cầu rõ nhất và reachable qua academic network | Med |
| **SOM** | 6B – 12B VND/năm (12-24 tháng) | 200–500 tổ chức × 200K VND/tháng × 12 tháng. Dựa trên adoption rate 1-2%/tháng của SAM, benchmark B2B SaaS VN | Low |

### Top 3 Unknowns

1. **Willingness to pay:** Career advisors tại ĐH công lập có ngân sách mua tool SaaS không? Cần pilot validate.
2. **Data freshness requirement:** User cần data real-time (hàng ngày) hay weekly aggregate đã đủ?
3. **Competitive response:** Nếu TopCV tự build insight dashboard, switching cost có đủ cao không?

### Judgment: ✅ Worth pursuing now
- Khoảng trống rõ ràng (không ai phục vụ career advisor)
- Chi phí build thấp (team 3 người, LLM API rẻ)
- Thị trường đủ lớn cho Seed round

---

<!-- TRANG 4: CUSTOMER + PAIN STATEMENT -->

## Trang 4 — Customer & Pain Statement (Day 16–17)

### Customer Segment Card

| | |
|---|---|
| **Segment name** | Career advisors tại trường ĐH và trung tâm tuyển dụng tại VN |
| **Operational context** | Mỗi tuần phải tư vấn cho 20–50 sinh viên/ứng viên về hướng đi nghề nghiệp, skill cần học, ngành nào đang tuyển |
| **Recurring workflow** | Mở 5-6 tab (TopCV, VietnamWorks, LinkedIn, ITviec) → duyệt JD → copy số liệu → tổng hợp vào Excel → rút insight → tư vấn |
| **Pain moment** | Giữa buổi tư vấn, sinh viên hỏi "Skill Python hay React đang hot hơn?" — advisor không có data để trả lời chính xác, phải nói "để cô/thầy kiểm tra lại" |
| **Why now** | Thị trường tuyển dụng VN thay đổi nhanh hơn giáo trình. Advisor mất uy tín nếu insight cũ 3-6 tháng. LLM API mới đủ rẻ để build tool aggregate |
| **Access path** | Qua mạng lưới academic (hội thảo career counseling, nhóm Facebook advisor, partnership với phòng đào tạo ĐH) |

### Need Map

**Need #1 (Priority):**
- **JTBD:** When career advisors cần tổng hợp xu hướng thị trường trước buổi tư vấn, they want tra cứu nhanh bằng câu hỏi tự nhiên, so they can trả lời sinh viên chính xác với dữ liệu có nguồn thay vì phỏng đoán.
- **Current workaround:** Mở 5-6 tab, duyệt JD thủ công, copy vào Excel.
- **Pain signal:** Mất 5-8 giờ/tuần. Insight cũ → tư vấn lệch hướng → sinh viên mất niềm tin.
- **Evidence:** Các nền tảng hiện tại (TopCV, VietnamWorks) chỉ phục vụ job seeker matching, không aggregate insight cho advisor. AICC (FPTU) từng thử nhưng đã ngừng hoạt động.

**Need #2:**
- **JTBD:** When career advisors cần chia sẻ insight thị trường với trưởng khoa hoặc doanh nghiệp đối tác, they want export báo cáo chuyên nghiệp, so they can chứng minh giá trị tư vấn bằng data.
- **Current workaround:** Tự soạn slide PowerPoint, screenshot biểu đồ từ nhiều nguồn.
- **Pain signal:** Mất 2-3 giờ/báo cáo. Không chuyên nghiệp. Data không nhất quán.

---

<!-- TRANG 5: PRD SUMMARY + PMF -->

## Trang 5 — PRD Summary & PMF Metric (Day 17)

### MVP Boundary

| | |
|---|---|
| **Killer Feature** | Chatbot Agent trả lời thị trường lao động bằng ngôn ngữ tự nhiên, kèm trích dẫn nguồn JD gốc |
| **Riskiest Assumption** | "Career advisors sẵn sàng dùng AI chatbot thay vì tự tra cứu thủ công — và tin tưởng insight aggregate hơn cảm nhận cá nhân" |

**In-Scope (MVP):**
1. Chatbot Agent — hỏi thị trường bằng ngôn ngữ tự nhiên, trả lời kèm citation
2. Market Dashboard — 6 KPI cards + line chart xu hướng skill
3. Export PDF — báo cáo thị trường tự động

**Out-of-Scope:**
- CV upload + gap analysis
- Personalized career roadmap
- Real-time salary negotiation tool
- Mobile native app

**Non-Goals:**
- Thay thế career advisor (chỉ hỗ trợ, không tự động tư vấn)
- Hiển thị raw JD content (chỉ aggregate + link gốc — ADR-10)

### AI-Specific Design

| | |
|---|---|
| **Model** | OpenRouter (Gemini Flash / GPT-4o-mini) — chi phí thấp, đủ chất lượng cho summarization + tool calling. Trade-off: accuracy thấp hơn GPT-4o, chấp nhận được cho aggregate insight |
| **Data Source** | JD crawl từ TopCV, LinkedIn, Indeed, ITviec, VietnamWorks. Polite crawling (rate limit, robots.txt). Chỉ metadata + link — không lưu full JD (ADR-10) |
| **Fallback UX** | Human-in-the-loop: AI disclaimer "Dữ liệu tổng hợp, có thể chưa đầy đủ" + link nguồn gốc để user verify. Confidence thấp → "Không đủ dữ liệu để trả lời chính xác, vui lòng kiểm tra nguồn gốc" |

### PMF Metric

| | |
|---|---|
| **Aha Moment** | Advisor hỏi chatbot → nhận insight kèm trích dẫn nguồn → **sử dụng insight đó trong buổi tư vấn tiếp theo** |
| **Actionable Metric** | % advisors sử dụng Agent ≥ 3 lần/tuần (retention-based, không phải sign-up count) |
| **PMF Method** | Sean Ellis Test — target > 40% "Very disappointed" nếu không còn dùng được |
| **Vanity Metrics KHÔNG dùng** | Số lượt đăng ký, page views, tổng messages |

---

<!-- TRANG 6: FINANCIAL MODEL — ASSUMPTIONS -->

## Trang 6 — Financial Model Assumptions (Day 18)

### Revenue Model: Hybrid (Base fee + Overage)

| | Optimistic | Base | Pessimistic |
|---|---:|---:|---:|
| **ARPU** | 300K VND/tháng | 200K VND/tháng | 150K VND/tháng |
| **TAM (segment)** | 5.000 advisors | 5.000 advisors | 5.000 advisors |
| **Adoption rate** | 2%/tháng | 1%/tháng | 0.5%/tháng |
| **Monthly Churn** | 3% | 5% | 8% |

### Cost Structure

| | Optimistic | Base | Pessimistic |
|---|---:|---:|---:|
| **API cost/user/tháng** | 15K VND | 20K VND | 30K VND |
| **Hidden costs** (labeling, retraining, QA) | 5K VND | 8K VND | 12K VND |
| **Infrastructure/user/tháng** | 5K VND | 7K VND | 10K VND |
| **→ Tổng COGS/user/tháng** | 25K VND | 35K VND | 52K VND |
| **→ Gross Margin** | 92% | 83% | 65% |

### Customer Acquisition

| | Optimistic | Base | Pessimistic |
|---|---:|---:|---:|
| **CAC** | 200K VND | 350K VND | 600K VND |

### Fixed Costs (tháng)

| | Optimistic | Base | Pessimistic |
|---|---:|---:|---:|
| **Salaries (3 người)** | 30M VND | 36M VND | 45M VND |
| **Office + tools** | 3M VND | 5M VND | 7M VND |
| **Marketing budget** | 5M VND | 8M VND | 12M VND |
| **→ Tổng Fixed/tháng** | 38M VND | 49M VND | 64M VND |

### Investment

| | |
|---|---|
| **Vốn đầu tư ban đầu** | 200M VND (MVP build + setup) |
| **Tiền mặt sau đầu tư (seed)** | 300M VND |
| **Discount rate (WACC)** | 22%/năm |

### Decision Note

> ARPU 200K VND/tháng dựa trên benchmark B2B SaaS tool tại VN (tương đương 1 bữa ăn trưa/tháng — ngưỡng chấp nhận cho tool chuyên biệt tại ĐH). CAC 350K dựa trên academic channel (hội thảo + referral) — rẻ hơn nhiều so với digital ads B2C. Churn 5% cao hơn benchmark B2B (2%) vì user academic có thể dùng theo học kỳ, không liên tục. Hidden costs 8K/user/tháng = ~40% API cost — bao gồm data labeling cho skill extraction và QA output.

---

<!-- TRANG 7: UNIT ECONOMICS -->

## Trang 7 — Unit Economics: LTV / CAC / Payback (Day 18)

### Unit Economics Summary

| Metric | Optimistic | Base | Pessimistic |
|---|---:|---:|---:|
| **Gross Margin/user/tháng** | 275K VND | 165K VND | 98K VND |
| **Số tháng ở lại** (1/Churn) | 33 tháng | 20 tháng | 12.5 tháng |
| **LTV** | 9.075K VND | 3.300K VND | 1.225K VND |
| **CAC** | 200K VND | 350K VND | 600K VND |
| **LTV/CAC** | **45.4x** ✅ | **9.4x** ✅ | **2.0x** 🟡 |
| **CAC Payback** | 0.7 tháng ✅ | 2.1 tháng ✅ | 6.1 tháng ✅ |

### Verdict

| Scenario | LTV/CAC > 3? | CAC Payback < 12? | Status |
|---|---|---|---|
| **Optimistic** | ✅ 45.4x | ✅ 0.7 tháng | ✅ HEALTHY |
| **Base** | ✅ 9.4x | ✅ 2.1 tháng | ✅ HEALTHY |
| **Pessimistic** | 🟡 2.0x | ✅ 6.1 tháng | 🟡 WATCHLIST |

> **Base case healthy.** Pessimistic chưa đạt LTV/CAC > 3 — cần giảm churn (cải thiện retention) hoặc tăng ARPU (thêm premium tier). Đây là risk cần monitor chặt.

---

<!-- TRANG 8: ROADMAP + OKRs -->

## Trang 8 — Roadmap Now/Next/Later + OKRs (Day 20)

### Roadmap Now / Next / Later

| Cột | Vấn đề | Sẽ làm |
|---|---|---|
| **NOW** | Career advisors chưa có kênh hỏi nhanh thị trường — mất hàng giờ tự tổng hợp | Tích hợp Chatbot Agent với Backend API thật (hybrid search + citations) |
| **NOW** | Insight vô nghĩa nếu data JD rời rạc, schema chưa thống nhất | Hoàn thiện JD Crawl Pipeline (Medallion: Bronze → Silver → Gold), polite crawling |
| **NEXT** | Advisor cần bức tranh tổng quan bằng biểu đồ — không phải ai cũng muốn chat | Kết nối Dashboard với real aggregate data, điều chỉnh KPIs theo data thật |
| **NEXT** | Researcher muốn chia sẻ insight với stakeholders nhưng phải tự soạn slide | Polish Export PDF với real data + preview trước download |
| **LATER** | Phân tích title-based bỏ lỡ nuance — hard-code không phân biệt skill weight | Skill Extraction Agent (AI reasoning). *Có thể bỏ* nếu keyword matching đủ 70% |
| **LATER** | User muốn đối chiếu CV cá nhân với thị trường | CV gap analysis (matching pipeline có prototype). *Có thể bỏ* |

> **Không có ngày tháng.** Chỉ thứ tự ưu tiên. NOW xong → NEXT bắt đầu.

### OKRs — Quý tới

**Objective:** Trở thành công cụ nghiên cứu thị trường lao động không thể thiếu cho career advisors và HR tại Việt Nam

| KR | Loại | Target | 70% Sweet Spot |
|---|---|---|---|
| **KR1** | Leading | 50 advisors dùng Agent ≥ 3 lần/tuần | ~35 advisors |
| **KR2** | Lagging | 200 báo cáo tải về bởi 30+ tổ chức | ~140 báo cáo × 21 tổ chức |
| **KR3** | Quality | NPS ≥ 40, churn ≤ 15%/tháng | NPS ~28, churn ~20% |

---

<!-- TRANG 9: DEPENDENCY MAP + CRITICAL PATH -->

## Trang 9 — Dependency Map + Critical Path (Day 20)

### 3 External Dependencies

| # | Dependency | Tier | Worst-case | Plan B | Cost |
|---|---|---|---|---|---|
| 1 | **OpenRouter / LLM API** | 🔴 Tier 1 | Rate limit siết hoặc giá tăng 5x → chatbot down | Abstraction layer (`llm_client.py` có). Switch Gemini/Claude trong 24h. Redis caching top 50 queries. | 2 tuần dev |
| 2 | **MongoDB Atlas + Qdrant** | 🔴 Tier 1 | Outage hoặc free tier hết quota → backend 500 error | `InMemoryJobRepository` fallback **đã có code**. Backup JSON daily. FAISS local cho vector search. | 0 ngày fallback |
| 3 | **Nền tảng tuyển dụng** (TopCV, LinkedIn, Indeed) | 🟡 Tier 2 | Block IP / đổi HTML → không crawl được JD mới | Multi-source strategy (5 nền tảng). Public datasets (Kaggle). RSS/API public. User-submitted JD. | 7 ngày |

### Cascading Failure

> Nếu LLM + DB fail cùng lúc: InMemoryRepo (12 fixtures) + Redis cache → chatbot trả lời ~30% queries cơ bản. **Single point of failure:** Supabase Auth — cần guest mode hoặc email/password fallback.

### Critical Path

```
Legal Compliance → JD Crawl Pipeline → Data Normalize → MongoDB Import → API Integration → Launch
     (ADR-10)        (multi-source)     (Bronze→Silver    (Silver→Gold     (Frontend ↔
                                          →Gold)           + Qdrant)        Backend)
```

**6 task tuần tự — trễ 1 ngày trên critical path = trễ launch 1 ngày.**

**Non-critical (parallel, có buffer):** UI Polish, i18n refinement, Export PDF polish, Documentation, Deployment setup.

> **Focus: Toàn bộ engineering effort vào Legal → Crawl → Normalize → Import → API.**

---

## Phụ lục — Links

| Tài liệu | Link |
|---|---|
| GitHub Repository | [A20-App-116](https://github.com/) |
| README — System Architecture & Flow | `README.md` |
| WORKLOG — ADR + Sprint tracking | `WORKLOG.md` |
| JOURNAL — Weekly learning log | `JOURNAL.md` |
| RICE Matrix | `rice_matrix.md` |
| Roadmap Now/Next/Later | `roadmap_nnl.md` |
| OKRs | `okrs.md` |
| Dependency Map | `dependency_map.md` |

---

*Package prepared by Team A20 — AI Career Advisor Assistant*
*"Vision without execution is just hallucination." — Thomas Edison*
