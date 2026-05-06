# Day 20 — Sổ tay học viên
## Roadmap & Execution
### Kế hoạch sinh tồn của AI startup

> **Vision without execution is just hallucination.**
> Tầm nhìn không có thực thi — chỉ là ảo giác. — Thomas Edison

---

## 0. Cách dùng sổ tay này

Dùng **trong lúc làm 4 workshops** — không phải để đọc hết một lượt. Mỗi lần bí, mở đúng phần cần:

| Khi bạn cần… | Mở phần… |
|---|---|
| Hiểu mạch logic tổng thể | §1 |
| Đọc nhanh một khái niệm (RICE/OKR/Dependency...) | §2 |
| Hướng dẫn từng bước workshop | §3 |
| Chạy AI để giúp prioritize / viết OKR / tìm dependency | §4 (Prompts) |
| Biết output gì cần có ở mỗi checkpoint | §5 (Checkpoints) |
| Xem tiêu chí chấm điểm & cách submit | §6 (Rubric & Submission) |
| Đọc tham khảo sâu hơn | §7 (References) |

**Quy ước ngôn ngữ:** Tiếng Việt ưu tiên. Các **term, công thức, prompt** giữ tiếng Anh để chuẩn ngành và không lệch nghĩa khi làm việc với AI.

---

## 1. Mạch logic Day 20

Day 20 trang bị 4 framework để biết **làm gì trước, làm gì sau, đo bằng gì, rủi ro ở đâu**:

```
       Cửa 1: Có 100 ý tưởng — chọn 5 nào? (RICE)
                      ↓
       Cửa 2: Sắp xếp thế nào? (Now/Next/Later)
                      ↓
       Cửa 3: Đo bằng gì để biết đúng hướng? (OKRs)
                      ↓
       Cửa 4: Rủi ro ngoài tầm kiểm soát? (Dependency)
                      ↓
              MILESTONE 1 PACKAGE
              (gộp Day 16-20)
```

### Tại sao Day 20 quan trọng?

Day 19 các bạn đã pitch xong với AI VC. Tưởng tượng đã gọi vốn thành công 500 triệu VND seed. **Đây mới là lúc cơn ác mộng thật sự bắt đầu:**

> Tech Co-founder muốn xây model to. Đội Sales đòi tính năng dễ bán. CEO muốn pivot theo trend. User phản hồi 100 ý tưởng. Investor hỏi roadmap. **5 demand cùng lúc, từ 5 nhóm khác nhau.**

Nếu lao vào code tất cả → **tiền cạn trước khi sản phẩm ra đời**. Đây là cách 70% AI startup chết.

Day 20 dạy cách quyết định khoa học — không cảm tính.

### 4 case studies & 4 framework

| Block | Câu hỏi | Framework | Case study |
|---|---|---|---|
| **1. Chọn hành trang** | Làm gì trước? | RICE + 2x2 Matrix | Intercom 2015 |
| **2. Vẽ bản đồ** | Sắp xếp thế nào? | Now/Next/Later | ProdPad & Janna Bastow |
| **3. Đặt cột mốc** | Đo bằng gì? | OKRs | Google Chrome 2008 |
| **4. Cạm bẫy ký sinh** | Rủi ro ở đâu? | Dependency Map + Critical Path | AI Legal startup |

### Output cuối buổi

**Milestone 1 Investor Package** — gộp 5 ngày Day 16-20 thành 1 bộ hồ sơ Seed Round duy nhất. Đây là **tấm vé thông hành** để các bạn đi gọi vốn ngoài đời thực.

---

## 2. Các khái niệm chính

### 2.1 Output vs Outcome

> **Shift mindset quan trọng nhất Day 20:** *Outcome over Output.*

Đây là căn bệnh trầm kha của founder dân tech.

| | **Output (BAD)** | **Outcome (GOOD)** |
|---|---|---|
| Đo gì? | Số features ship, dòng code, accuracy | Giá trị user nhận được |
| Ngôn ngữ | Developer | Business |
| Ví dụ | "Em ship 12 features tháng này" | "User tiết kiệm 1.7 giờ/ngày" |
| | "Model accuracy 99.7%" | "Doanh số khách +18%" |
| | "Code coverage 95%" | "Churn giảm từ 8% xuống 3%" |
| VC nghĩ gì? | "Có ai dùng không?" | "Đây là business thật" |

**Bài học:** Output không trả lời được câu *"có ai dùng không?"*. Outcome thì có.

---

### 2.2 RICE Framework

Sinh ra năm 2015 bởi Sean McBride tại Intercom — vì ông không chịu nổi cãi vã trong phòng họp roadmap.

**Insight cốt lõi:** *Cảm tính tạo cãi vã. Toán học tạo quyết định.*

#### Công thức

$$
\text{RICE Score} = \frac{R \times I \times C}{E}
$$

#### 4 yếu tố

| Yếu tố | Câu hỏi | Đơn vị |
|---|---|---|
| **R — Reach** | Bao nhiêu user/quý sẽ đụng tính năng? | Số người |
| **I — Impact** | Tác động đến user mạnh cỡ nào? | 0.25 / 0.5 / 1 / 2 / 3 |
| **C — Confidence** | Tự tin về R, I bao nhiêu %? | 50% / 80% / 100% |
| **E — Effort** | Tốn bao nhiêu person-month? | Person-month |

#### Impact scale

| Score | Ý nghĩa | Ví dụ |
|---|---|---|
| 0.25 | tiny | Đổi màu nút |
| 0.5 | low | Thêm filter trong dashboard |
| 1 | medium | Thêm export CSV |
| 2 | high | Auto-reply giảm 2h/ngày |
| 3 | massive | Voice AI biến shop thành brand |

#### Confidence — quan trọng nhất

> **Quy tắc nghiêm:** Confidence chưa từng test = **50% MAX**. Không có ngoại lệ.

| Đã làm gì? | Confidence |
|---|---|
| Chưa interview ai | 50% |
| Interview 5-10 user xác nhận | 80% |
| Có pilot data thật | 100% |

#### 3 lỗi phổ biến khi chấm RICE

| Lỗi | Pattern | Fix |
|---|---|---|
| **Confidence ảo** | "Em chấm 100% dù chưa test" | Chưa test = 50% MAX |
| **Reach lạc quan** | "100% user sẽ dùng" | Discount 50% (Mixpanel benchmark: chỉ 20-40% dùng) |
| **Effort underestimate** | "2 tuần là xong" | Multiply 1.5x (cộng QA, bug fix, integration) |

#### Ví dụ — ShopReplyAI

| Tính năng | R | I | C | E | Score |
|---|---|---|---|---|---|
| Auto-reply Shopee | 5000 | 2.0 | 0.8 | 2 | **4000** |
| Voice cloning shop owner | 1000 | 3.0 | 0.5 | 6 | **250** |
| Sentiment analysis | 2000 | 0.5 | 0.8 | 3 | **267** |
| Multi-language | 500 | 1.0 | 1.0 | 4 | **125** |
| A/B test templates | 3000 | 1.0 | 0.9 | 1 | **2700** |

**Đọc kết quả:** Top 2 ưu tiên: **Auto-reply (4000)** và **A/B test (2700)** → làm trước. **Voice cloning** điểm thấp dù Impact cao — vì Effort 6 tháng và Confidence chỉ 50%.

> **Bài học:** Tính năng cool không nhất thiết là tính năng đáng làm trước.

---

### 2.3 2x2 Value-Effort Matrix

Sau khi có RICE score → ném features vào ma trận 2x2.

```
              Effort
            Low         High
          ┌────────┬────────┐
     High │ Quick  │Strategic│
          │  Wins  │  Bets   │
   Value  ├────────┼────────┤
     Low  │Fill-ins│  Non-   │
          │        │starters │
          └────────┴────────┘
```

| Quadrant | Đặc điểm | Chiến lược | Ví dụ |
|---|---|---|---|
| **Quick Wins** | High value + Low effort | Làm ngay — lấy đà | A/B test templates |
| **Strategic Bets** | High value + High effort | Đầu tư dài hạn = moat | Auto-reply integration |
| **Fill-ins** | Low value + Low effort | Làm khi rảnh | Sentiment dashboard |
| **Non-starters** | Low value + High effort | **VỨT** vào sọt rác | Voice cloning |

**Pro tip:**
- **Quick Wins** build momentum và trust với team. VC thấy bạn ship nhanh.
- **Strategic Bets** build moat dài hạn. Pitch để raise Series A.
- **Non-starters** là cái VC ghét nhất khi thấy trong roadmap. Signal: founder không biết prioritize.

---

### 2.4 Now / Next / Later Framework

Sinh ra từ vụ trả giá đắt của **Janna Bastow** (founder ProdPad) — cô cam kết deadline với khách enterprise, đêm trước launch bug critical xuất hiện, ship buggy product → **mất \$50K contract**.

**Insight cốt lõi:** *Roadmap không phải contract — là la bàn.*

#### 3 cột

| Cột | Đặc điểm | Thời gian | Câu nói |
|---|---|---|---|
| **NOW** | Đang code hôm nay. Chi tiết cao. Rủi ro thấp. | 1-3 tháng | "Tuần này dev đang code feature X" |
| **NEXT** | Sẽ làm sau NOW. Chi tiết medium. Rủi ro trung bình. | 3-6 tháng | "Sau khi NOW xong sẽ làm Y" |
| **LATER** | Tầm nhìn dài hạn. Mơ hồ. Rủi ro cao. | 6-18 tháng | "Một ngày nào đó sẽ build Z" |

#### Quy tắc vàng

1. **KHÔNG ngày tháng cụ thể.** Chỉ thứ tự ưu tiên.
2. **Mỗi ô là *vấn đề* (problem), không phải *tính năng* (feature).**

#### Tại sao problem-statement?

- **Problem stable hơn solution.** Solution có thể đổi theo tech mới — problem thì không.
- **Engineering creative hơn.** Họ tự nghĩ ra solution tốt hơn — không bị bound bởi solution founder áp đặt.
- **Customer-facing.** Khi share roadmap với customer, họ relate với problem — không quan tâm tech specifics.

#### Cái bẫy Gantt Chart

| | Gantt Chart | Now/Next/Later |
|---|---|---|
| Format | Timeline cứng với deadline | 3 cột không deadline |
| Hứa hẹn | "15/8 ra mắt" | "Sau khi NOW xong" |
| Khi bug critical xuất hiện | Ship buggy hoặc trễ hạn → mất trust | OK trễ — vẫn giữ chất lượng |
| Phù hợp với | Manufacturing, construction | Phần mềm, AI startup |

> **Trong AI: model hallucinate, API sập, data bẩn. Bất định là tuyệt đối.** Bạn không bao giờ đoán đúng ngày.

#### Ví dụ — ShopReplyAI

| Cột | Vấn đề | Sẽ làm |
|---|---|---|
| **NOW** | 50 shop pilot đang dùng AI auto-reply, nhưng chỉ chạy được trên Shopee | Integration với TikTok Shop + chuyển từ webhook sang real-time WebSocket. Dự kiến 2 tháng |
| **NEXT** | Shop owner cần insight về câu hỏi nào AI trả lời tốt, câu nào kém | Analytics dashboard + sentiment analysis. Bắt đầu khi NOW xong |
| **LATER** | Shop owner muốn AI trả lời voice messages | Voice AI agent. Cần research thêm — chi phí ASR + TTS với Vietnamese accent chưa rõ. Có thể bỏ |

---

### 2.5 OKRs (Objectives and Key Results)

Sinh ra ở Intel năm 1970s, được John Doerr mang sang Google năm 1999. **Sundar Pichai dùng OKR để biến Chrome từ 0 → 3 tỷ user.**

**Insight cốt lõi:** *OKR không phải KPI để đánh giá performance. OKR là cái la bàn — giúp biết khi nào cần đổi chiến lược.*

#### Cấu trúc

```
        1 Objective
            +
       3 Key Results
```

| | **Objective (O)** | **Key Results (KRs)** |
|---|---|---|
| **Đặc điểm** | Định tính, ngắn, nhớ được | Định lượng, có số |
| **Số lượng** | 1 per quarter | 3 per Objective (sweet spot) |
| **Câu hỏi** | "Chúng ta đi đâu?" | "Làm sao biết đã đến?" |
| **Ví dụ** | "Trở thành tool AI reply số 1 cho SME e-commerce VN" | "Đạt 200 paying shop" |

#### Quy tắc 70%

> Hoàn thành 100% KR = **set lần sau cao hơn**, không phải khen.

OKR là *aspirational target* — set cao hơn 30-50% than safely achievable. Hoàn thành 60-70% là sweet spot.

Khác KPI truyền thống là *committed target* — phải đạt 100%.

#### OKR cho AI startup — Bad vs Good

❌ **BAD: Output-focused**
```
Objective: Build AI product tốt nhất
KR1: Model accuracy đạt 95%
KR2: Ship 12 features trong quý
KR3: Code coverage 90%
```
**Vấn đề:** User KHÔNG quan tâm accuracy. Họ quan tâm tiết kiệm bao nhiêu giờ. KR đo cái user không care.

✅ **GOOD: Outcome-focused (Leading + Lagging + Quality)**
```
Objective: Trở thành tool AI reply không thể thiếu của SME e-commerce VN

KR1 (Leading):  100 paying shop pilot dùng app ≥ 5 ngày/tuần
KR2 (Lagging):  MRR đạt 500M VND, tăng 50% so với Q3
KR3 (Quality):  NPS ≥ 50, churn ≤ 3%/tháng
```

#### 3 loại Key Results

| Loại | Đo gì? | Ví dụ |
|---|---|---|
| **Leading** | User behavior — predict future. Sửa kịp. | DAU, retention week-1, activation rate |
| **Lagging** | Business metric — confirm result | MRR, paying customer, ARR |
| **Quality** | Bảo vệ growth bền vững | NPS, churn rate, retention |

> **Pro tip:** Mỗi OKR phải có 1 Leading + 1 Lagging + 1 Quality. Bao quát toàn diện business health.

---

### 2.6 Dependency Map

Mỗi external dependency là một cái dao treo trên đầu — có thể rơi bất kỳ lúc nào.

> *99% AI startup hiện nay là ký sinh trùng. Họ không sở hữu tài sản gì.*

#### Bạn đang ký sinh trên ai?

| Sản phẩm AI | Ký sinh trên... | Nếu họ thay đổi |
|---|---|---|
| AI chatbot | OpenAI/Anthropic API | API down = product down |
| AI image generator | Stable Diffusion / Replicate | Pricing 5x = margin về 0 |
| AI sales tool | HubSpot / Salesforce data | Họ thu hồi access = không có data |
| AI CRM extension | Chrome browser | Google đổi extension policy |
| AI voice assistant | Deepgram / Whisper | Latency tăng = UX hỏng |

#### 3 Tier Dependencies

| Tier | Đặc điểm | Ai? | Mitigation |
|---|---|---|---|
| **🔴 Tier 1 — Critical** | Có thể giết bạn trong 1 ngày | OpenAI/Anthropic API, AWS/GCP | Multi-vendor, abstraction layer, multi-region |
| **🟡 Tier 2 — Important** | Có thể giết trong 1 tuần đến 1 tháng | Apple/Google Play, Twilio/Stripe | Web fallback, comply day-1, abstract layer |
| **⚪ Tier 3 — Watch** | Cần aware | Browser stores, data sources | Direct download fallback, B2B contracts |

#### Quy tắc cốt lõi

> **Mỗi Tier 1 dependency phải có Plan B sẵn sàng deploy trong 24 giờ.**

Plan B không phải document. Là **code đã viết, đã test, sẵn sàng switch**. Khi crisis — không có thời gian code Plan B từ đầu.

> **Nếu không có Plan B — đó không phải startup, đó là kinh doanh nhà thuê.**

#### Câu chuyện cảnh báo: AI Legal startup

- Pilot 6 tháng với 3 firm luật. Pitch deck đẹp. VC interested với \$500K SAFE.
- Chủ Nhật đêm: OpenAI siết rate limit GPT-4 từ 500 req/min → 50 req/min, **effective immediately**.
- Sản phẩm tóm tắt 1 tài liệu pháp lý 50 trang = 80 GPT-4 calls = **20 phút/document** (trước đây 30 giây).
- Sáng thứ Hai: 47 ticket support "app không trả lời". Lawyer chửi qua phone.
- VC pause SAFE. **Phá sản 4 tháng sau.**

**Bài học:** Họ làm RICE đầy đủ, viết OKR, vẽ Gantt. Bỏ qua **1 thứ duy nhất**: Dependency Map.

---

### 2.7 Critical Path

Khái niệm classic từ project management: **trễ 1 ngày trên Critical Path = trễ launch 1 ngày**.

#### Cơ chế

Trong dự án có 2 loại task:
- **Critical tasks** — tuần tự, không thể parallel. Trễ 1 cái = trễ tất cả
- **Non-critical tasks** — có buffer time. Trễ 1 ngày không sao

#### Critical Path điển hình của AI startup

```
Data Pipeline → Legal Compliance → Model Fine-tune → API Integration → Launch
```

5 bước tuần tự. Không thể parallel.

#### Non-critical (đường xám, có buffer)

- UI/UX Design — có thể parallel với Legal Compliance
- Marketing Site — có thể làm trong khi Model fine-tune
- Documentation — có thể làm sau cùng
- Analytics setup — có thể làm trong khi API integration

#### Ý nghĩa thực tế

> **Khi có pressure thời gian — focus toàn bộ engineering effort vào Critical Path.**

Đừng cho engineer làm UI polish khi Data Pipeline chưa xong. Đừng làm Marketing Site khi Legal Compliance chưa clear.

> **Trong AI startup: Data Pipeline và Legal Compliance hầu như luôn nằm trên Critical Path.** Đó là 2 task founder thường underestimate nhất.

---

### 2.8 Milestone 1 Investor Package

Bộ hồ sơ Seed Round gộp 5 ngày Day 16-20 — *tấm vé thông hành* để gọi vốn ngoài đời thực.

#### 5 thành phần

| # | Tài liệu | Từ |
|---|---|---|
| 1 | Market Analysis + PRD (Customer + Pain + Solution) | Day 16-17 |
| 2 | Financial Model + Unit Economics (LTV, CAC, Payback) | Day 18 |
| 3 | Investor Pitch Deck (Twitter Pitch + Pitch Memo) | Day 19 |
| 4 | Roadmap Now/Next/Later + OKRs (1 quý) | Day 20 |
| 5 | Dependency Map + Critical Path | Day 20 |

#### Cấu trúc PDF — 9 trang

| Trang | Nội dung |
|---|---|
| 1 | Cover + Executive Summary (Twitter Pitch) |
| 2-5 | Pitch Memo (1 trang) + Market + PRD summary |
| 6-7 | Financial Model + Unit Economics |
| 8 | Roadmap + OKRs |
| 9 | Dependency Map + Critical Path |
| Phụ lục | Link đến file Excel chi tiết Day 18, file PRD đầy đủ Day 17 |

> **9 trang. Không hơn.** VC chỉ đọc 2.5 phút mỗi deck — long PDF = pass.

---

## 3. 4 Workshop — Hướng dẫn chi tiết

### 3.1 Workshop 1 — Chấm RICE (15 phút)

**Output:** Bảng RICE 5 dòng + 2x2 Value-Effort Matrix.

#### 4 bước

**Bước 1.** Mở PRD Day 17. Chọn **5 tính năng cốt lõi**. Không hơn, không kém.

**Bước 2.** Cho mỗi tính năng, chấm:

| Yếu tố | Quy tắc |
|---|---|
| **Reach** | Số user/quý sẽ đụng. Discount 50% so với optimistic estimate |
| **Impact** | 0.25 / 0.5 / 1 / 2 / 3 |
| **Confidence** | Chưa test = 50% MAX |
| **Effort** | Person-month. Multiply 1.5x estimate ban đầu |

**Bước 3.** Tính score = $(R × I × C) / E$.

**Bước 4.** Vẽ 2x2 Value-Effort. Xác định:
- 1 **Quick Win** — làm trước
- 1 **Strategic Bet** — moat dài hạn
- 1 **Non-starter** — bỏ thẳng

#### Pass/Fail signals

| Pass ✅ | Fail ❌ |
|---|---|
| Có ít nhất 1 feature Confidence < 80% | Tất cả Confidence 100% |
| Có Non-starter rõ ràng | Tất cả features đều OK |
| Effort discounted realistic | Effort tất cả = 1-2 tuần |
| Có Quick Win + Strategic Bet rõ | Chỉ có Quick Wins (thiếu vision) |

---

### 3.2 Workshop 2 — Now/Next/Later (15 phút)

**Output:** Roadmap Now/Next/Later 1 trang.

#### Quy trình

Lấy bảng RICE từ Workshop 1. Sắp xếp 5 tính năng vào 3 cột:

| Cột | Quy tắc | Số vấn đề |
|---|---|---|
| **NOW** | Quick Wins từ 2x2 + RICE score cao nhất | 1-3 vấn đề |
| **NEXT** | Strategic Bets từ 2x2 | 2-4 vấn đề |
| **LATER** | Vision lớn, có thể chưa technically khả thi | 1-2 vấn đề lớn |

#### Quy tắc nghiêm

- **KHÔNG ghi ngày tháng** — không "tháng 8", không "Q2"
- **Mỗi ô viết là *vấn đề* cần giải, không phải *tính năng***
- Format: "Vấn đề: ... / Sẽ làm: ..."

#### Template

```markdown
## NOW
**Vấn đề:** [Pain mà user đang gặp]
**Đang code:** [Solution + estimated duration]

## NEXT
**Vấn đề:** [Next pain to solve]
**Sẽ làm:** [High-level direction]

## LATER
**Vấn đề:** [Big vision pain]
**Có thể làm:** [Mention "có thể bỏ" if chưa chắc]
```

#### Pass/Fail signals

| Pass ✅ | Fail ❌ |
|---|---|
| Mỗi cột là vấn đề, không phải tính năng | "Tháng 8 launch feature X" |
| NOW có 1-3 vấn đề (không quá tải) | NOW liệt kê 8 features |
| LATER honest "có thể bỏ" | LATER cam kết chắc chắn |
| Không có ngày tháng | Có deadline cụ thể |

---

### 3.3 Workshop 3 — Viết OKR cho NOW (15 phút)

**Output:** 1 Objective + 3 Key Results.

#### Quy trình

Nhìn cột **NOW** trong roadmap (Workshop 2). Viết OKR cho 1 quý tới.

**Bước 1.** Viết **1 Objective**:
- Định tính, không số
- Truyền cảm hứng (founder muốn đọc to mỗi sáng)
- Match với vấn đề ở cột NOW

**Bước 2.** Viết **3 Key Results** theo khung Leading + Lagging + Quality:

| KR | Loại | Ví dụ |
|---|---|---|
| **KR1** | Leading (dự báo) | User behavior metric — DAU, retention week-1, activation rate |
| **KR2** | Lagging (kết quả) | Revenue/business metric — MRR, paying customer count |
| **KR3** | Quality | NPS, retention rate, churn |

#### Quy tắc nghiêm

- **KHÔNG dùng từ kỹ thuật** — không model, API, latency
- **KHÔNG đo Output** — không số features, code lines
- Phải có **con số cụ thể** mỗi KR
- Áp dụng quy tắc 70% — KR aspirational, không safely achievable

#### Pass/Fail signals

| Pass ✅ | Fail ❌ |
|---|---|
| Objective truyền cảm hứng | Objective chỉ là tagline marketing |
| Mỗi KR có số cụ thể | "Tăng nhiều" / "Cải thiện" |
| Đủ 3 loại Leading/Lagging/Quality | 3 KR cùng loại (vd 3 revenue metric) |
| KR aspirational 1.5-2x baseline | KR safely achievable hoặc 10x ảo |
| Ngôn ngữ business | "Model accuracy" / "Latency < 100ms" |

---

### 3.4 Workshop 4 — Dependency Map (15 phút)

**Output:** 3 dependencies + Plan B + Critical Path 1 trang.

#### Quy trình

**Bước 1.** Liệt kê **3 external dependencies** có thể giết dự án trong 30 ngày tới.

Ví dụ điển hình:
- OpenAI/Anthropic API rate limit hoặc pricing change
- Apple App Review reject hoặc ban
- GDPR audit nếu sản phẩm cho EU
- Shopee/Lazada API access nếu integrate
- AWS region down nếu deploy single-region

**Bước 2.** Với mỗi dependency, viết:

| Mục | Yêu cầu |
|---|---|
| **Worst-case scenario** | 1 câu mô tả cái xấu nhất |
| **Plan B** | Cụ thể — code đã viết, có thể deploy trong 7 ngày |
| **Cost** | Tiền + thời gian implement Plan B |

**Bước 3.** Vẽ Critical Path đơn giản:
- Liệt kê 5-7 task chính cho NOW
- Đánh dấu task nào blocking task khác
- Highlight chuỗi dài nhất = Critical Path

#### Template Plan B

```markdown
## Dependency 1: OpenAI API rate limit/pricing
**Worst-case:** OpenAI siết rate limit hoặc tăng giá 5x đột ngột.
**Plan B:** Code abstraction layer cho LLM. Switch sang Claude (Anthropic)
  hoặc Gemini trong 24h. Caching layer cho 70% queries thường gặp.
**Cost:** 2 tuần dev (đã build Plan B chưa? Bao giờ build?)
```

#### Pass/Fail signals

| Pass ✅ | Fail ❌ |
|---|---|
| Plan B cụ thể với vendor + cost | Plan B generic "tìm cách khác" |
| Có Plan B cho mọi Tier 1 dependency | Chỉ phụ thuộc OpenAI, không có fallback |
| Critical Path có Legal Compliance | Critical Path bỏ qua legal/compliance |
| UI/Marketing parallel với Critical | UI design nằm trên Critical Path |

---

### 3.5 Đóng gói Milestone 1 Package (25 phút)

**Output:** `[Tên]_Milestone1_InvestorPackage.pdf` — 9 trang.

#### Quy trình đóng gói

1. **Tạo PDF** từ markdown hoặc Google Docs.
2. **Cấu trúc 9 trang** theo template:

```
Trang 1:    Cover + Executive Summary (Twitter Pitch từ Day 19)
Trang 2:    Pitch Memo 1-pager (Day 19)
Trang 3:    Market Analysis (Day 16)
Trang 4:    Customer + Pain Statement (Day 16-17)
Trang 5:    PRD Summary + PMF Metric (Day 17)
Trang 6:    Financial Model — Assumptions (Day 18)
Trang 7:    Unit Economics — LTV/CAC/Payback (Day 18)
Trang 8:    Roadmap Now/Next/Later + OKRs (Day 20 Workshop 2 + 3)
Trang 9:    Dependency Map + Critical Path (Day 20 Workshop 4)
```

3. **Phụ lục** — link đến:
   - File Excel chi tiết Day 18
   - File PRD đầy đủ Day 17
   - GitHub repo nếu có

#### Pass/Fail signals

| Pass ✅ | Fail ❌ |
|---|---|
| 9 trang đầy đủ | Quá 15 trang |
| Twitter Pitch ngay trang 1 | Phải lật đến trang 5 mới hiểu sản phẩm |
| Có numbers cụ thể (LTV, CAC, MRR) | Generic "tăng đáng kể" |
| Có dependency + Plan B | Không nhắc external risks |
| Visual sạch, không text dày đặc | Block of text 100% |

---

## 4. Prompts cho Vibe Coding (English-only)

> **Lưu ý:** Tất cả prompt giữ tiếng Anh 100% để AI giữ ngữ nghĩa ổn định. Thảo luận kết quả bằng tiếng Việt.

### 4.1 RICE Score Sanity Check

Dùng sau Workshop 1 — kiểm tra bảng RICE của bạn có realistic không.

```
Act as a senior product manager who has been chairing prioritization
meetings at Stripe for 5 years. You've seen every type of inflated
RICE score.

Below is my RICE matrix for an AI startup:

[paste your 5-feature RICE table]

Critique it ruthlessly on 4 dimensions:

1. CONFIDENCE INFLATION
   Which features have Confidence ≥ 80% but no real user validation?
   Force me to downgrade if I haven't interviewed 5+ users.

2. REACH OPTIMISM
   Which Reach numbers feel inflated? Apply Mixpanel benchmark:
   only 20-40% of users adopt new features in first quarter.
   Suggest realistic discount.

3. EFFORT UNDERESTIMATE
   Which Effort estimates are missing QA, integration testing,
   and post-launch monitoring? Apply 1.5x multiplier where needed.

4. STRATEGIC BLINDSPOT
   Looking at my top 2 RICE scores — are they actually building
   moat for the long term, or just chasing quick wins?
   Should I add a Strategic Bet that scores lower but builds
   defensibility?

For each issue, suggest the corrected score with reasoning.
```

---

### 4.2 Now/Next/Later Roadmap Generator

Dùng khi Workshop 2 đang bí — không biết phân loại features vào cột nào.

```
I'm building [your AI product]. Help me draft a Now/Next/Later
roadmap.

Context:
- Target customer: [describe]
- Current stage: [pilot with X users / pre-launch / post-launch]
- Current pain points users report: [list 3-5]
- Top RICE features (from my Workshop 1):
  1. [feature + RICE score]
  2. [feature + RICE score]
  ...

Generate a Now/Next/Later roadmap following these rules:

1. Each cell describes a PROBLEM (not a feature)
2. NO calendar dates — only priority order
3. NOW: 1-3 problems we're solving this quarter
4. NEXT: 2-4 problems for next 3-6 months (when NOW is done)
5. LATER: 1-2 visionary problems (might be cut)

For each cell, write:
- "Vấn đề:" describing user pain
- "Sẽ làm:" describing high-level approach (not detailed spec)

Then explain WHY each problem is in that cell — what evidence
supports the priority?
```

---

### 4.3 OKR Critique & Rewrite

Dùng sau Workshop 3 — đảm bảo OKR của bạn outcome-focused, không output-focused.

```
Act as a startup advisor who has reviewed 100+ Series A pitch
decks this year. You're tired of generic OKRs that VCs immediately
discount.

Here's my OKR for next quarter:

OBJECTIVE: [your objective]

KR1: [your KR1]
KR2: [your KR2]
KR3: [your KR3]

Critique on 5 dimensions:

1. OUTPUT vs OUTCOME
   Which KRs measure shipping (output) vs user value (outcome)?
   Quote the specific KR and explain.

2. LEADING / LAGGING / QUALITY MIX
   Do my 3 KRs cover: user behavior (leading), revenue (lagging),
   and health (quality)? If missing one, suggest what to add.

3. ASPIRATIONAL CALIBRATION
   Apply the 70% rule. Are my targets:
   - Too easy (would hit 100%)?
   - Too aspirational (would hit 0%)?
   Suggest the ~70% sweet spot for each KR.

4. JARGON CHECK
   Quote any technical jargon (model, API, latency, accuracy)
   that should be replaced with business language.

5. INVESTOR-READINESS
   If I read this OKR to a Sequoia partner in 30 seconds,
   would they:
   (a) Get excited about the vision?
   (b) Trust the metrics?
   Score 1-10 with reasoning.

Then provide a rewritten version that addresses all issues.
```

---

### 4.4 Dependency Risk Assessment

Dùng sau Workshop 4 — stress-test Plan B của bạn.

```
Act as a CTO who survived the OpenAI rate limit crisis of 2024.
You've seen 3 AI startups die because they had no fallback.

Here are my 3 external dependencies and Plan Bs:

DEPENDENCY 1: [name]
- Worst-case: [your scenario]
- Plan B: [your fallback]
- Cost: [your estimate]

[same for DEPENDENCY 2, 3]

Stress-test on 5 dimensions:

1. TIER CLASSIFICATION
   Is each dependency correctly classified as Tier 1 (1 day kill),
   Tier 2 (1 week kill), or Tier 3 (watchlist)?
   Be specific about the kill speed.

2. PLAN B SPECIFICITY
   Is each Plan B:
   (a) Specific to a vendor (e.g., "switch to Claude")?
   (b) Has working code already, or just a doc?
   (c) Deployable in <24 hours?
   Score each: ready / partial / not-yet-built.

3. HIDDEN DEPENDENCIES
   What dependencies am I missing? Common blindspots:
   - Tokenizer / embeddings vendor
   - Authentication providers (Auth0, Clerk)
   - Analytics (Mixpanel, Amplitude)
   - Email delivery (SendGrid)
   List any I should add.

4. CASCADING FAILURES
   If Tier 1 dependency #1 fails AND #2 fails simultaneously,
   does my Plan B chain still work?
   Identify single points of failure.

5. ECONOMIC IMPACT
   For each dependency, estimate:
   - Revenue loss per day if it fails
   - User trust loss (qualitative)
   - VC perception if they hear about the failure

Be brutally honest. I'd rather know now than at the partner meeting.
```

---

### 4.5 Critical Path Analyzer

Dùng để verify Critical Path của bạn — task nào thực sự blocking, task nào có buffer.

```
I have these tasks for next quarter (cột NOW):

[paste 5-7 tasks from your Workshop 4]

For each task, tell me:

1. DEPENDENCIES
   Which other tasks must complete BEFORE this can start?
   List them as "Task X depends on: A, B, C".

2. PARALLEL OPPORTUNITIES
   Which tasks can run in parallel with each other?
   Group them as "Parallel cluster: [task list]".

3. CRITICAL PATH
   What is the longest sequence of dependent tasks?
   Format: Task A → Task B → Task C → ... → Launch
   This is my Critical Path.

4. BUFFER TASKS
   Which tasks have slack time (could be delayed without
   affecting launch)? List as "Buffer tasks: [list]".

5. RISK ANALYSIS
   For each task on Critical Path:
   - What could delay it by 1+ weeks?
   - What's my mitigation strategy?

6. AI STARTUP SPECIFIC
   In AI startups, Data Pipeline and Legal Compliance usually
   sit on Critical Path. Did I include them? If not, where
   should they fit?

Output a clear ASCII diagram of dependencies + Critical Path,
plus a list of bufferable tasks.
```

---

### 4.6 Investor Package Reviewer

Dùng sau khi đóng gói Milestone 1 Package — nhận feedback trước khi gửi VC thật.

```
Act as a Partner at Y Combinator who reviews 50 Seed Round packages
per week. You spend 2.5 minutes per package on average. You decide
in 8 seconds whether to keep reading.

Below is my 9-page Milestone 1 Investor Package:

[paste your package, or describe each page]

Critique it as if you were deciding whether to schedule a call:

1. THE 8-SECOND TEST (Page 1)
   Did the cover/executive summary grab my attention?
   What's the ONE number that should be on page 1 and isn't?

2. THE FLOW
   Does the package follow the natural reading order?
   Problem → Solution → Traction → Ask → Risk?
   What's misordered?

3. THE NUMBERS DEFENSIBILITY
   Which numbers (LTV, CAC, MRR, growth rate) feel inflated
   or unsupported? What questions would I ask in due diligence?

4. THE MOAT
   After reading all 9 pages, can I articulate the team's
   defensibility in 1 sentence? If not, what's missing?

5. THE RISK TRANSPARENCY
   Did the founders honestly discuss external risks (OpenAI
   dependency, regulatory, competitive)?
   Or did they hide them? Honest risks = trust signal.

6. THE ASK CLARITY
   Is the ask specific (amount + use of funds + 12-month milestones)?
   Or vague?

7. THE PASS/PROCEED DECISION
   Based on this package alone — would I:
   (a) Schedule a 30-min intro call?
   (b) Pass with a polite "not for us"?
   (c) Forward to a junior partner for further review?

   Give your honest decision with 3 reasons.

Be harsh. I'd rather you tell me than a real VC ghost me.
```

---

## 5. Checkpoints — Output yêu cầu

### 5.1 Checkpoint 1 — RICE Matrix (cuối Block 1, 10:00)

**Output:** `rice_matrix.md` — bảng RICE 5 dòng + 2x2 Matrix.

**Pass signals:**
- 5 features cụ thể từ PRD Day 17
- Confidence chấm honest (không 100% mass)
- Có Quick Win + Strategic Bet + Non-starter rõ ràng
- Effort discounted realistic

**Fail signals:**
- "Cảm tính" thay vì numbers
- Tất cả Confidence 100%
- Tất cả features cùng quadrant
- Effort tất cả là 1-2 tuần

---

### 5.2 Checkpoint 2 — Roadmap (cuối Block 2, 10:45)

**Output:** `roadmap_nnl.md` — Now/Next/Later 1 trang.

**Pass signals:**
- Mỗi ô là vấn đề (problem), không phải tính năng (feature)
- KHÔNG có ngày tháng
- NOW có 1-3 vấn đề (không quá tải)
- LATER có honest "có thể bỏ"

**Fail signals:**
- "Tháng 8 launch feature X"
- NOW liệt kê 8+ features
- LATER cam kết chắc chắn
- Mọi ô đều là tên feature

---

### 5.3 Checkpoint 3 — OKRs (cuối Block 3, 11:45)

**Output:** `okrs.md` — 1 Objective + 3 Key Results.

**Pass signals:**
- Objective truyền cảm hứng, không số
- 3 KR cover Leading + Lagging + Quality
- Mỗi KR có số cụ thể
- KR aspirational (~70% sweet spot)
- Ngôn ngữ business, không tech

**Fail signals:**
- "Model accuracy 95%"
- "Ship 12 features"
- "Code coverage 90%"
- 3 KR cùng loại (vd: 3 revenue metric)
- KR mơ hồ "tăng đáng kể"

---

### 5.4 Checkpoint 4 — Dependency Map (cuối Block 4, 12:30)

**Output:** `dependency_map.md` — 3 dependencies + Plan B + Critical Path.

**Pass signals:**
- 3 dependencies cụ thể với vendor name
- Plan B có cost (tiền + thời gian)
- Plan B deployable trong 7 ngày
- Critical Path có Legal Compliance + Data Pipeline

**Fail signals:**
- Plan B generic "tìm cách khác"
- Chỉ phụ thuộc OpenAI, không có fallback model
- Critical Path bỏ qua legal
- UI design nằm trên Critical Path

---

### 5.5 Final — Milestone Package (cuối Block 5, 13:00)

**Output:** `milestone1_package.pdf` — 9 trang đầy đủ.

**Pass signals:**
- 9 trang theo template
- Twitter Pitch ngay trang 1
- Có tất cả 5 thành phần
- Visual sạch, không dày đặc text
- Có numbers cụ thể (LTV, CAC, MRR, etc.)

**Fail signals:**
- > 15 trang
- Phải lật đến trang 5 mới hiểu sản phẩm
- Generic "tăng trưởng nhanh" thay vì numbers
- Block of text 100%
- Thiếu Dependency hoặc OKR section

---

### 5.6 Final Checklist — Trước 13:00

```
[ ] 1. rice_matrix.md         — 5 features RICE + 2x2 Matrix
[ ] 2. roadmap_nnl.md         — Now/Next/Later 1 trang
[ ] 3. okrs.md                — 1 Objective + 3 KRs
[ ] 4. dependency_map.md      — 3 deps + Plan B + Critical Path
[ ] 5. milestone1_package.pdf — Bộ hồ sơ 9 trang gộp Day 16-20
[ ] 6. Test mở PDF — render đẹp, không lỗi font
[ ] 7. Nén ZIP: [Tên]_Day20.zip
[ ] 8. Nộp LMS trước 13:00
```

**Minimum bar:** Nếu một Lead Partner Y Combinator mở Milestone Package của bạn lúc 9h sáng (cùng 100 deck khác), họ sẽ:
- **Đọc hết 9 trang** trong 2.5 phút?
- **Hiểu** product + traction + ask?
- **Schedule 30-min intro call** sau khi đọc?

Nếu trả lời CÓ cho cả 3 — Package của bạn pass.

---

## 6. Rubric & Submission

### 6.1 Cách nộp bài

Day 20 chỉ có **1 phiên bản nộp duy nhất**:

| Mục | Yêu cầu |
|---|---|
| **Nộp khi nào** | Cuối buổi sáng Day 20 — **trước 13:00** |
| **Nộp ở đâu** | Submit trực tiếp trên LMS |
| **Tên file** | `[Tên]_Day20.zip` |
| **Bao gồm** | 5 files trong 1 thư mục |

> **KHÔNG có BTVN.** Day 20 hoàn tất trong buổi sáng. Đây là milestone cuối Chương 4.

---

### 6.2 Rubric — 100 điểm, 5 tiêu chí

| # | Tiêu chí | Điểm |
|---|---|---:|
| 1 | **Prioritization Quality** (RICE + 2x2) | 20 |
| 2 | **Roadmap Clarity** (Now/Next/Later) | 20 |
| 3 | **OKR Outcome Focus** | 20 |
| 4 | **Risk Awareness** (Dependency + Critical Path) | 20 |
| 5 | **Investor Package Polish** | 20 |

---

#### Tiêu chí 1 — Prioritization Quality (20 điểm)

Chấm chất lượng RICE matrix + 2x2.

- ✓ 5 features cụ thể từ PRD
- ✓ Confidence honest (chưa test = ≤ 50%)
- ✓ Reach discounted realistic
- ✓ Effort multiplied 1.5x
- ✓ 2x2 phân biệt rõ Quick Win / Strategic Bet / Non-starter

**Điểm cao nhất:** RICE matrix có ít nhất 1 Confidence ≤ 50% — chứng tỏ founder honest về uncertainty.

---

#### Tiêu chí 2 — Roadmap Clarity (20 điểm)

Chấm Now/Next/Later format.

- ✓ Mỗi ô là vấn đề (problem), không phải tính năng (feature)
- ✓ KHÔNG có ngày tháng
- ✓ NOW có 1-3 items (focused)
- ✓ NEXT có 2-4 items (medium horizon)
- ✓ LATER có honest disclaimer "có thể bỏ"

**Điểm cao nhất:** Roadmap có thể đọc cho non-technical mentor và họ relate được — vì problem-statement.

---

#### Tiêu chí 3 — OKR Outcome Focus (20 điểm)

Chấm OKR có outcome-focused không.

- ✓ Objective định tính, không số, truyền cảm hứng
- ✓ 3 KR đủ Leading + Lagging + Quality
- ✓ Mỗi KR có số cụ thể
- ✓ KR aspirational (~70% sweet spot)
- ✓ Ngôn ngữ business, không tech jargon

**Điểm cao nhất:** Một VC đọc OKR có thể đoán đúng business model của startup chỉ qua 4 dòng.

---

#### Tiêu chí 4 — Risk Awareness (20 điểm)

Chấm Dependency Map + Critical Path.

- ✓ 3 dependencies cụ thể với vendor name
- ✓ Plan B có cost (tiền + thời gian)
- ✓ Plan B deployable trong 7 ngày
- ✓ Critical Path identify Data + Legal + Model + API + Launch
- ✓ Non-critical tasks identify đúng (UI/marketing có buffer)

**Điểm cao nhất:** Có ít nhất 1 *cascading failure* analysis — "nếu OpenAI fail VÀ AWS fail cùng lúc, plan B chain còn work không?"

---

#### Tiêu chí 5 — Investor Package Polish (20 điểm)

Chấm chất lượng Milestone 1 Package PDF.

- ✓ 9 trang theo template
- ✓ Twitter Pitch ngay trang 1
- ✓ Tất cả 5 thành phần đầy đủ
- ✓ Visual sạch, không dày đặc text
- ✓ Numbers cụ thể (LTV, CAC, MRR, etc.)

**Điểm cao nhất:** Package có thể gửi cho real VC ngay tuần sau — không cần edit thêm.

---

### 6.3 Grade bands

| Band | Điểm | Ý nghĩa |
|---|---:|---|
| Outstanding | 90–100 | Có thể fundraise ngay với package này |
| Strong | 75–89 | Cần 1 round refine với mentor |
| Pass | 60–74 | Hiểu framework, package còn rough |
| Needs rework | 40–59 | Sai concept core (output thay vì outcome, no plan B) |
| Fail | <40 | Chưa đạt minimum bar |

---

### 6.4 Lưu ý khi làm bài

- **Đừng skip 2x2 Matrix.** Chỉ RICE table không đủ — cần visual quadrants.
- **Đừng ghi ngày tháng** trong NOW/NEXT/LATER. Mất ngay 5 điểm.
- **Đừng dùng tech jargon** trong OKR. Mất ngay 5 điểm Tiêu chí 3.
- **Đừng để Plan B generic.** "Tìm cách khác" = không có Plan B.
- **Critical Path phải có Legal Compliance** cho AI startup. Đa số founder bỏ qua.
- **Package PDF phải dưới 12 trang.** Long PDF = VC pass.
- **Trang 1 phải có Twitter Pitch.** VC chỉ đọc 8 giây slide đầu.

---

## 7. References

### Core readings

1. **Intercom — RICE Framework**
   https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/
   Sean McBride bài viết gốc 2015 — RICE đã được industry-standardize.

2. **ProdPad — Why I Invented the Now-Next-Later Roadmap**
   https://www.prodpad.com/blog/invented-now-next-later-roadmap/
   Janna Bastow kể câu chuyện trả giá vì Gantt Chart, sáng tạo NNL.

3. **Google re:Work — OKRs Guide**
   https://rework.withgoogle.com/intl/en/guides/set-goals-with-okrs/
   Google's official guide cho OKR — base case study Chrome.

4. **Measure What Matters — John Doerr**
   Sách kinh điển về OKR. Từng được Larry Page và Sundar Pichai endorse.

### Further reading (optional)

5. **Inspired — Marty Cagan**
   Chương về prioritization và outcome-focused product management.

6. **The Lean Startup — Eric Ries**
   Background cho concept "validated learning" → liên quan Confidence trong RICE.

7. **Critical Path Method (PMI)**
   Project management classic, foundational cho Critical Path concept.

8. **OpenAI Rate Limit Documentation**
   https://platform.openai.com/docs/guides/rate-limits
   Hiểu thực tế dependency on foundation model.

### Quick reference — câu chốt Day 20

| Câu chốt |
|---|
| "Vision without execution is just hallucination." — Edison |
| "Có tiền rồi — bài toán mới bắt đầu." |
| "Outcome over Output." |
| "Cảm tính tạo cãi vã. Toán học tạo quyết định." |
| "Confidence chưa test = 50% MAX." |
| "Tính năng cool không nhất thiết là tính năng đáng làm trước." |
| "Roadmap không phải contract — là la bàn." |
| "Mỗi ô là vấn đề, không phải tính năng." |
| "OKR không phải KPI — là la bàn." |
| "Mỗi Tier 1 dependency phải có Plan B sẵn sàng deploy trong 24 giờ." |
| "Không có Plan B — không phải startup, là kinh doanh nhà thuê." |
| "From idea → to package → to round." |

---

*Chúc các bạn execute không hallucinate — from product → to package → to round.*
