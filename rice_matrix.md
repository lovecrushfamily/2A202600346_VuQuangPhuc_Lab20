# Workshop 1 — RICE Matrix + 2x2 Value-Effort Matrix

## Sản phẩm: AI Career Advisor Assistant (A20)

> **Insight:** "Cảm tính tạo cãi vã. Toán học tạo quyết định." — RICE Framework, Intercom 2015

---

## Bảng RICE — 5 Tính năng cốt lõi

| # | Tính năng | Reach (user/quý) | Impact | Confidence | Effort (person-month) | RICE Score |
|---|---|---:|---:|---:|---:|---:|
| 1 | **Chatbot Agent — hỏi thị trường bằng ngôn ngữ tự nhiên** | 500 | 2.0 | 0.8 | 2 | **400** |
| 2 | **Market Dashboard — biểu đồ KPI + line chart xu hướng** | 400 | 2.0 | 0.5 | 1.5 | **267** |
| 3 | **Export PDF — báo cáo thị trường tự động** | 200 | 1.0 | 0.8 | 0.5 | **320** |
| 4 | **JD Crawl Pipeline tự động (multi-source, scheduled)** | 300 | 3.0 | 0.5 | 4.5 | **100** |
| 5 | **Skill Extraction Agent — trích kỹ năng từ JD description bằng AI** | 250 | 3.0 | 0.5 | 6 | **63** |

---

## Giải thích chấm điểm

### Feature 1: Chatbot Agent
- **Reach = 500:** Ước tính 500 user (career advisors, sinh viên, HR) sẽ dùng trong quý đầu. Discount 50% từ 1.000 user tiềm năng vì sản phẩm mới, chưa có marketing mạnh.
- **Impact = 2.0 (High):** Giảm 2+ giờ/ngày nghiên cứu thủ công cho career advisors. Trả lời kèm trích dẫn nguồn — khác biệt với ChatGPT generic.
- **Confidence = 80%:** Edge function đã hoạt động trên Supabase, có 5 sprint phát triển. Agent core loop đã test với OpenRouter free models.
- **Effort = 2 person-month:** Cần tích hợp real backend API (thay mock), polish streaming, xử lý edge cases.

### Feature 2: Market Dashboard
- **Reach = 400:** HR, recruiters, researchers cần dashboard tổng quan. Discount 50% từ 800 vì chỉ subset user quan tâm data visualization.
- **Impact = 2.0 (High):** 6 KPI cards + line chart giúp nắm bắt xu hướng trong 30 giây thay vì tự tổng hợp.
- **Confidence = 50%:** Dashboard hiện dùng **mock data**. Chưa có real API pipeline. EDA cho thấy data thật khác xa mock (ADR-13). Chưa validate với user thật.
- **Effort = 1.5 person-month:** Component UI đã có, nhưng cần pipeline thật + real aggregate data + điều chỉnh KPIs cho khớp thực tế.

### Feature 3: Export PDF
- **Reach = 200:** Chỉ subset career advisors và researchers cần export — HR thường dùng dashboard trực tiếp. Discount 50% từ 400.
- **Impact = 1.0 (Medium):** Tiện lợi để chia sẻ với stakeholders, nhưng không phải tính năng mà user dùng hàng ngày.
- **Confidence = 80%:** `jspdf` + `html2canvas` đã hoạt động, output PDF chạy được. Cần polish font và dark mode.
- **Effort = 0.5 person-month:** Phần lớn đã xong. Chỉ cần thay mock data bằng real data khi pipeline sẵn sàng.

### Feature 4: JD Crawl Pipeline tự động
- **Reach = 300:** Gián tiếp ảnh hưởng mọi user qua chất lượng data. Nhưng user không "đụng" trực tiếp — reach tính theo số user hưởng lợi.
- **Impact = 3.0 (Massive):** Không có data pipeline = không có sản phẩm. Đây là nền tảng cho mọi tính năng khác.
- **Confidence = 50%:** Đã crawl ~4.000 JD links nhưng chất lượng rất khác nhau giữa các nguồn. LinkedIn noise cao (ADR-13). Schema chưa thống nhất. Legal compliance chưa clear hoàn toàn (ADR-10).
- **Effort = 4.5 person-month:** Multi-source crawler (TopCV, LinkedIn, Indeed) + polite crawling + normalize + Medallion pipeline (Bronze → Silver → Gold) + scheduling + monitoring. Multiply 1.5x từ estimate ban đầu 3 tháng.

### Feature 5: Skill Extraction Agent
- **Reach = 250:** Subset của pipeline users. Chỉ hữu ích khi đã có đủ JDs — gián tiếp.
- **Impact = 3.0 (Massive):** Biến raw JD thành structured skill data — "React 40%, Python 35%" thay vì chỉ title matching. Moat dài hạn.
- **Confidence = 50%:** Chưa có prototype. Cần reasoning phức tạp ("proficiency in Python" vs "Python is a plus" có weight khác nhau — ghi chú từ ADR-13). Chưa test accuracy.
- **Effort = 6 person-month:** Cần thiết kế Agent/tool chuyên biệt, training data, evaluation framework, integration với pipeline. Multiply 1.5x từ estimate 4 tháng.

---

## 2x2 Value-Effort Matrix

```
                     Effort
                Low              High
          ┌──────────────┬──────────────┐
          │              │              │
   High   │  QUICK WINS  │  STRATEGIC   │
          │              │    BETS      │
  Value   │  ✅ Export    │  🎯 JD Crawl │
          │     PDF      │   Pipeline   │
          │  ✅ Chatbot  │              │
          │    Agent     │              │
          ├──────────────┼──────────────┤
          │              │              │
   Low    │  FILL-INS    │ NON-STARTERS │
          │              │              │
          │  📊 Market   │  ❌ Skill    │
          │  Dashboard*  │  Extraction  │
          │              │    Agent     │
          │              │              │
          └──────────────┴──────────────┘

* Dashboard value = Low hiện tại vì chưa có real data.
  Sẽ chuyển lên High khi pipeline sẵn sàng.
```

---

## Phân tích

### ✅ Quick Wins — Làm ngay
1. **Export PDF (RICE: 320)** — Effort thấp nhất, đã gần xong. Ship nhanh, build trust.
2. **Chatbot Agent (RICE: 400)** — Score cao nhất. Core value proposition. Tích hợp real backend API là ưu tiên #1.

### 🎯 Strategic Bet — Đầu tư dài hạn (Moat)
- **JD Crawl Pipeline (RICE: 100)** — Score thấp vì Effort cao + Confidence chỉ 50%. Nhưng đây là **foundation** của mọi tính năng khác. Không có pipeline = không có data = không có sản phẩm. Đầu tư vì moat.

### 📊 Fill-in — Làm khi rảnh
- **Market Dashboard (RICE: 267)** — Score khá nhưng Confidence chỉ 50% (mock data). Cần pipeline thật trước. Hiện tại giữ mock, đợi data rồi mới polish.

### ❌ Non-starter — Bỏ (hiện tại)
- **Skill Extraction Agent (RICE: 63)** — Score thấp nhất. Impact massive (3.0) nhưng Effort 6 tháng + Confidence 50%. Cần research riêng. Đây là tính năng cool **nhưng không đáng làm trước** — đúng bài học "tính năng cool ≠ tính năng đáng ưu tiên."

---

## Kết luận

> **Top 2 ưu tiên:** Chatbot Agent (400) + Export PDF (320) → ship ngay, lấy đà.
>
> **Strategic Bet:** JD Crawl Pipeline (100) → đầu tư dài hạn, nền tảng cho mọi thứ.
>
> **Bỏ:** Skill Extraction Agent (63) → vision hay nhưng chưa đúng lúc.
