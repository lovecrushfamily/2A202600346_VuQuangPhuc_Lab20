# Workshop 3 — OKRs (Objectives & Key Results)

## Sản phẩm: AI Career Advisor Assistant (A20)

> "OKR không phải KPI — là la bàn."

---

## Objective

> **Trở thành công cụ nghiên cứu thị trường lao động không thể thiếu cho career advisors và HR tại Việt Nam**

---

## Key Results — Quý tới

### KR1 — Leading (User Behavior)

> **50 career advisors và HR dùng Chatbot Agent ít nhất 3 lần/tuần để tra cứu thị trường**

- **Đo:** Số người dùng active quay lại — signal sản phẩm hữu ích
- **Tại sao 50?** Hiện 0 user thật. 50 pilot users aspirational nhưng khả thi nếu target career advisors tại ĐH và trung tâm tuyển dụng
- **70% rule:** Sweet spot = ~35 users × 3 lần/tuần

### KR2 — Lagging (Business Metric)

> **Đạt 200 báo cáo thị trường được tải về (Export PDF) bởi ít nhất 30 tổ chức khác nhau**

- **Đo:** Revenue proxy — advisor download báo cáo để chia sẻ = giá trị đủ lớn để "mang đi show"
- **Tại sao 200?** 50 users × 4 báo cáo/quý = 200
- **70% rule:** Sweet spot = ~140 báo cáo × 21 tổ chức

### KR3 — Quality (Bảo vệ growth)

> **NPS ≥ 40 từ survey pilot users, tỉ lệ bỏ dùng (churn) ≤ 15%/tháng**

- **Đo:** Sự hài lòng — user có giới thiệu cho đồng nghiệp không?
- **Tại sao NPS 40?** Benchmark B2B SaaS sớm: 30–50. Dưới 30 = chưa đủ giá trị
- **70% rule:** Sweet spot = NPS ~28 + churn ~20%

---

## Kiểm tra chất lượng

| Tiêu chí | Pass? |
|---|---|
| Objective truyền cảm hứng, không số | ✅ |
| 3 KR cover Leading + Lagging + Quality | ✅ |
| Mỗi KR có số cụ thể | ✅ 50/3/200/30/40/15% |
| KR aspirational (~70%) | ✅ |
| Ngôn ngữ business, không tech | ✅ Không model/API/latency |
| Không đo output | ✅ Đo user behavior, downloads, satisfaction |

---

### ❌ BAD (đã tránh)
```
Objective: Hoàn thiện AI Career Advisor
KR1: Tích hợp 5 API endpoints
KR2: Model accuracy đạt 90%
KR3: Ship dashboard + export PDF
```

### ✅ GOOD (đã chọn)
```
Objective: Trở thành công cụ NCTT lao động không thể thiếu
KR1 (Leading):  50 advisors dùng ≥ 3 lần/tuần
KR2 (Lagging):  200 báo cáo tải về bởi 30+ tổ chức
KR3 (Quality):  NPS ≥ 40, churn ≤ 15%/tháng
```
