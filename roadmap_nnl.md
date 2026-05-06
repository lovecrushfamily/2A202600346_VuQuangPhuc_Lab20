# Workshop 2 — Roadmap Now / Next / Later

## Sản phẩm: AI Career Advisor Assistant (A20)

> **Insight:** "Roadmap không phải contract — là la bàn." — Janna Bastow, ProdPad

---

## NOW

> Tập trung giải quyết ngay. Chi tiết cao. Rủi ro thấp.

### Vấn đề 1: Career advisors và HR chưa có kênh hỏi nhanh để nắm xu hướng thị trường lao động — phải tự tổng hợp từ nhiều nguồn, mất hàng giờ mỗi tuần.

**Đang code:** Tích hợp Chatbot Agent với Backend API thật (FastAPI + MongoDB + Qdrant). Thay mock citations bằng real structured JSON từ hybrid search engine. Agent trả lời kèm trích dẫn nguồn (link JD gốc), không hiển thị raw JD. Ước tính 1–2 tháng để ổn định end-to-end.

### Vấn đề 2: Insight thị trường không có giá trị nếu dữ liệu JD chưa được thu thập, chuẩn hoá và cập nhật thường xuyên — hiện tại dữ liệu crawl còn rời rạc và schema chưa thống nhất giữa các nguồn.

**Đang code:** Hoàn thiện JD Crawl Pipeline tự động theo Medallion Architecture (Bronze → Silver → Gold). Chuẩn hoá schema từ TopCV, LinkedIn, Indeed vào MongoDB. Chạy polite crawling (rate limit, robots.txt — ADR-10). Sync data từ crawler vào MongoDB Bronze. Ước tính 2–3 tháng để pipeline chạy ổn định và scheduled.

---

## NEXT

> Giải quyết sau khi NOW xong. Chi tiết trung bình. Rủi ro trung bình.

### Vấn đề 3: Career advisors cần nhìn nhanh bức tranh tổng quan thị trường bằng biểu đồ và con số — không phải ai cũng muốn chat, nhiều người quen đọc dashboard.

**Sẽ làm:** Kết nối Market Dashboard với real aggregate data từ `/jobs` API. Điều chỉnh KPIs cho khớp data thật (EDA đã cho thấy mock data khác xa thực tế — ADR-13). Line chart demand index, top skills, top companies, salary range. Bắt đầu khi pipeline NOW đã có data ổn định.

### Vấn đề 4: Researchers và career advisors muốn chia sẻ insight thị trường với stakeholders (trưởng khoa, doanh nghiệp, sinh viên) — nhưng hiện tại phải screenshot hoặc tự soạn slide.

**Sẽ làm:** Polish Export PDF với real data: thay mock bằng aggregate thật, cải thiện font rendering, preview trước khi download. Output: `market-report-{range}-{date}.pdf` có cover, KPI summary, charts, tables, disclaimer.

---

## LATER

> Tầm nhìn dài hạn. Mơ hồ. Rủi ro cao.

### Vấn đề 5: Chỉ phân tích bằng tiêu đề JD (title-based) thì bỏ lỡ rất nhiều insight — "proficiency in Python" vs "Python is a plus" có weight hoàn toàn khác nhau, nhưng hard-code không phân biệt được.

**Có thể làm:** Xây Skill Extraction Agent — AI Agent chuyên biệt extract và phân loại kỹ năng từ description JD với reasoning. Cần training data, evaluation framework, prototype accuracy test. **Có thể bỏ** nếu hard-code bằng keyword matching đã đủ 70%+ insight cho target user hiện tại. Cần thêm research để quyết định.

### Vấn đề 6: User muốn phân tích gap giữa CV cá nhân và nhu cầu thị trường — upload CV → đối chiếu với thousands JD → đề xuất skill cần học.

**Có thể làm:** Tích hợp CV upload + matching pipeline (scorer, ranker, explainability đã có prototype ở backend). Cần user consent (GDPR-like), anonymization, production-grade accuracy. **Có thể bỏ** nếu MVP focus thuần vào market insight aggregate đã đủ giá trị.

---

## Tóm tắt

| Cột | Số vấn đề | Trọng tâm |
|---|---|---|
| **NOW** | 2 | Data pipeline + Chatbot Agent tích hợp thật |
| **NEXT** | 2 | Dashboard + Export PDF với real data |
| **LATER** | 2 | Skill Extraction Agent + CV Gap Analysis *(có thể bỏ)* |

> **Không có ngày tháng.** Chỉ có thứ tự ưu tiên. NOW xong → NEXT bắt đầu.
