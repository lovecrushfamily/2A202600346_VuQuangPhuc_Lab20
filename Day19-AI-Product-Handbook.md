# Day 19 — Sổ tay học viên
## Investor Buy-in & Pitch
### Gọi vốn cho AI Startup

> **A great AI product can still die from a bad pitch. A mediocre product CAN survive on a great pitch.**
> Sản phẩm AI tốt vẫn chết nếu pitch tệ. Sản phẩm trung bình vẫn sống nếu pitch tốt.

---

## 0. Cách dùng sổ tay này

Dùng **trong lúc làm Solo Pitch Lab** — không phải để đọc hết một lượt. Mỗi lần bí, mở đúng phần cần:

| Khi bạn cần… | Mở phần… |
|---|---|
| Hiểu mạch logic tổng thể | §1 |
| Đọc nhanh một khái niệm | §2 |
| Hướng dẫn từng bước Solo Pitch Lab | §3 |
| Chạy AI critique cho pitch của mình | §4 (Prompts) |
| Biết output gì cần có ở mỗi checkpoint | §5 (Checkpoints) |
| Xem tiêu chí chấm điểm & cách submit | §6 (Rubric & Submission) |
| Đọc tham khảo sâu hơn | §7 (References) |

**Quy ước ngôn ngữ:** Tiếng Việt ưu tiên. Các **term, công thức, prompt** giữ tiếng Anh để chuẩn ngành và không lệch nghĩa khi làm việc với AI.

---

## 1. Mạch logic Day 19

Day 19 trang bị 4 vũ khí để vượt qua 4 cửa ải sinh tồn của AI startup:

```
       Cửa 1: Ai nắm sinh mệnh startup của bạn?
                      ↓
       Cửa 2: 100 user đầu — vượt qua sự hoài nghi
                      ↓
       Cửa 3: Pitch chuẩn YC / Sequoia (280 ký tự)
                      ↓
       Cửa 4: Defend được pitch khi VC vặn vẹo?
```

### Tại sao Day 19 quan trọng?

Day 16-17-18 đã chuẩn bị cho bạn sản phẩm tốt + tài chính lành. Nhưng:

> **90% AI startups chết — không phải vì tech dở, mà vì *không ai cần* và *hết tiền*.**

Sản phẩm tốt + tài chính lành **vẫn không đủ** để sống. Bạn còn phải biết bán câu chuyện. Day 19 dạy điều đó.

### 4 blocks và đầu ra

| Block | Câu hỏi | Output |
|---|---|---|
| **1. Bản đồ hệ sinh thái** | Ai nắm sinh mệnh startup? | Mendelow Matrix với 4 quadrants |
| **2. Bán app Early Adopter** | Sao user không dùng app? | 3 archetypes + ADKAR + Hook |
| **3. The Twitter Pitch** | Pitch thế nào cho lọt tai VC? | Pitch Memo + Twitter Pitch (280 ký tự) |
| **4. Solo Pitch Lab** | Defend pitch được không? | Pitch đã pass qua AI VC critique |

---

## 2. Các khái niệm chính

### 2.1 Stakeholder Ecosystem — Hệ sinh thái startup

**Stakeholder:** *"Bất kỳ ai bị ảnh hưởng bởi startup của bạn — và có thể ảnh hưởng ngược lại."*

Founder thường chỉ nghĩ đến VC. Nhưng startup AI có ít nhất 6 nhóm stakeholder, mỗi nhóm có cách giết bạn riêng:

| Stakeholder | Họ quan tâm | Họ có thể giết bạn bằng cách... |
|---|---|---|
| **Co-founder** | Equity, vision, control | Bỏ đi giữa chừng, lấy IP |
| **Lead VC** | Return, milestones | Không follow-on round tiếp theo |
| **Early Adopters** | Lifestyle, ease of use | Review xấu trên Reddit/X |
| **Foundation Model API** (OpenAI...) | Compliance, ToS | Khóa API account |
| **Báo chí** | Story, drama | Đưa tin tiêu cực |
| **Cơ quan pháp lý** | Quy định, dữ liệu | Tuýt còi privacy/copyright |

**Bài học cốt lõi:** Founder thường chỉ nghĩ đến VC. **5 nhóm còn lại có thể giết startup nhanh hơn cả việc không gọi được vốn.**

---

### 2.2 Mendelow's Matrix — 4 quadrants

Công cụ kinh điển từ thập niên 90. Chia stakeholder vào 4 ô dựa trên 2 trục:
- **Power:** Họ có quyền lực bao nhiêu với startup?
- **Interest:** Họ quan tâm đến startup bao nhiêu?

```
                    Interest
              Low         High
            ┌────────┬────────┐
       High │  Keep   │ Manage │
            │Satisfied│ Closely│
   Power    ├────────┼────────┤
        Low │ Minimal │  Keep  │
            │ Effort  │Informed│
            └────────┴────────┘
```

**4 nhóm và chiến lược:**

| Quadrant | Đặc điểm | Ví dụ | Chiến lược |
|---|---|---|---|
| **Manage Closely** | High Power + High Interest | Lead VC, Co-founder | Họp hàng tuần, biến thành champion |
| **Keep Satisfied** | High Power + Low Interest | OpenAI, Apple, pháp lý | Đừng làm phiền, đừng chọc giận |
| **Keep Informed** | Low Power + High Interest | Early Adopters, beta tester | Build cộng đồng, cập nhật thường xuyên |
| **Minimal Effort** | Low Power + Low Interest | Đối thủ ngoài segment | Theo dõi nhẹ, không tốn time |

> **Quy tắc 60-20:** Founder dành **60% time** cho **20% stakeholder quan trọng nhất** (Manage Closely).

---

### 2.3 8 Power Players trong startup AI

| # | Thế lực | Quadrant phổ biến |
|---|---|---|
| 1 | **Lead VC** | Manage Closely |
| 2 | **Angel Investor** | Manage / Keep Informed |
| 3 | **Tech Co-founder** | Manage Closely |
| 4 | **Early Adopter** | Keep Informed |
| 5 | **Foundation Model API** | Keep Satisfied |
| 6 | **Đối thủ cạnh tranh** | Minimal Effort / Watch |
| 7 | **Báo chí AI** | Keep Informed (selective) |
| 8 | **Cơ quan pháp lý** | Keep Satisfied |

**Pro tip:** Quadrant phụ thuộc **loại sản phẩm AI** của bạn:

| Loại sản phẩm | Cơ quan pháp lý | OpenAI/Anthropic |
|---|---|---|
| AI Y tế / Tài chính | Manage Closely | Keep Satisfied |
| AI viết content | Minimal Effort | Keep Satisfied |
| AI agent dùng nhiều API | Minimal Effort | Manage Closely |
| AI on-device | Minimal Effort | Minimal Effort |

**Đừng copy-paste quadrant của startup khác. Tự đặt vào context của bạn.**

---

### 2.4 Why Users Don't Switch — 4 lý do user từ chối

> *"Người dùng không thiếu tool. Họ thiếu **lý do** để thay đổi thói quen."*

User đã có ChatGPT. App của bạn yêu cầu họ *thay đổi thói quen* — đó là rào cản tâm lý lớn nhất.

| # | Lý do | Câu user nói |
|---|---|---|
| 1 | **Switching cost** | "ChatGPT em dùng quen rồi, sao phải đổi?" |
| 2 | **Trust deficit** | "Startup này tồn tại được bao lâu? Dữ liệu của em có an toàn?" |
| 3 | **Friction onboarding** | "Phải đăng ký, verify email, chọn plan... mệt quá" |
| 4 | **Fear of replacement** | "Sếp thấy em dùng AI sẽ nghĩ em rảnh, đuổi em" |

**Bài pitch tốt cho user ≠ bài pitch tốt cho VC.** VC quan tâm tăng trưởng. User quan tâm *"tôi được lợi gì NGAY BÂY GIỜ"*. Hai ngôn ngữ khác nhau.

---

### 2.5 ADKAR Model — 5 bậc adoption

Khung change management chuẩn của Prosci. 5 bước user phải đi qua từ *biết* đến *dùng hằng ngày*:

| Bước | Câu user tự hỏi | Founder phải làm |
|---|---|---|
| **A**wareness | "Có app này à?" | Marketing, content, build-in-public |
| **D**esire | "Tại sao tôi quan tâm?" | **Story + WIIFM (What's In It For Me)** |
| **K**nowledge | "Nó hoạt động thế nào?" | Demo, video, docs |
| **A**bility | "Tôi dùng được không?" | Onboarding mượt, zero friction |
| **R**einforcement | "Tôi có quay lại mai không?" | Retention loop, habit hook |

#### Where founders fail

> **Đa số founder skip thẳng từ Awareness qua Ability.**
>
> Họ marketing → user click → thấy app → *không hiểu tại sao cần* → thoát.

**Desire là khoảng cách lớn nhất** trong ADKAR. Cũng là chỗ founder yếu nhất. Nếu nhớ một thứ về ADKAR — **nhớ chữ D**.

---

### 2.6 3 User Archetypes — 3 kiểu user khó tính nhất

Trong tệp khách hàng đầu, bạn sẽ gặp 3 archetype này. Bốc nhầm thuốc → user thoát app trong 30 giây.

#### Archetype 1: The Skeptic — Người hoài nghi

| | |
|---|---|
| **Câu nói** | "AI hay bịa chuyện. Data của tôi có lộ không?" |
| **Tắc ở** | Trust |
| **Chỗ thua trong ADKAR** | Awareness → Desire |
| **Nhân vật điển hình** | Senior dev, lawyer, healthcare professional |

**Thuốc giải — Minh bạch + Quyền kiểm soát:**

❌ **BAD:** Defensive về độ chính xác
> "Model em accuracy 99.7%, đã test 10,000 cases, đảm bảo không sai!"
> → Càng defensive càng nghi.

✅ **GOOD:** Acknowledge → Human-in-the-loop → Privacy concrete

1. **Acknowledge:** "Bạn đúng — AI có thể sai. Đó là lý do bọn em thiết kế thế này..."
2. **Human-in-the-loop:** "AI *không* tự động gửi email cho khách. Nó soạn nháp, bạn bấm Duyệt."
3. **Privacy concrete:**
   - "Data của bạn *không* được dùng để train model"
   - "Data lưu local hoặc tier riêng (không shared)"
   - "Bạn có thể export hoặc xóa toàn bộ data bất kỳ lúc nào"

> **Skeptic không sợ AI sai — họ sợ KHÔNG BIẾT khi nào AI sai. Cho họ quyền kiểm soát = giải tỏa nỗi sợ.**

---

#### Archetype 2: The Overloaded — Người quá tải

| | |
|---|---|
| **Câu nói** | "Đang chạy deadline, rảnh đâu mà học tool mới!" |
| **Tắc ở** | Time |
| **Chỗ thua trong ADKAR** | Knowledge → Ability |
| **Nhân vật điển hình** | PM, marketing manager, dịch vụ |

**Thuốc giải — Aha Moment trong 30 giây:**

❌ **BAD:** Onboarding 10 bước
> Sign up → Verify email → Phone OTP → Choose plan → Connect data → Tutorial → ...
> → User thoát ở bước 3.

✅ **GOOD:** Pattern "Try first — sign up later"

Ví dụ AI summary tool:
- User paste link YouTube ngay landing page (không cần sign up)
- Trong 5 giây thấy summary 3-bullet
- "Aha! Đỡ thật!"
- *Lúc đó* mới prompt sign up để save history

**Time-to-value:** dưới 30 giây.

**Ví dụ thực tế:**
- **Loom:** record màn hình ngay, sign up sau
- **Linear.app:** drag-drop demo board không cần account

> **Overloaded user trade attention cho value. Không có value trong 30s → thoát.**

---

#### Archetype 3: The Fearful — Người sợ hãi

| | |
|---|---|
| **Câu nói** | "Sếp thấy tôi dùng AI sẽ nghĩ tôi rảnh, đuổi tôi" |
| **Tắc ở** | Identity |
| **Chỗ thua trong ADKAR** | Desire (sợ hơn muốn) |
| **Nhân vật điển hình** | Junior staff, người ngành sắp bị disrupt |

**Thuốc giải — Superpower Narrative:**

❌ **BAD:** "AI tự động hóa 80% công việc"
> Marketing tagline: "Tự động hóa quy trình, giảm 80% nhân lực!"
> → Nhân viên đọc xong → "Sếp thấy tagline này sẽ đuổi tôi."
> → Phá hoại ngầm: *không* dùng tool dù sếp ép.

✅ **GOOD:** "AI làm bạn trở thành phiên bản nâng cấp"

**Reframe:** AI không thay thế người — *người biết dùng AI thay thế người không biết dùng*.

**Tagline mẫu:**
- "Trở thành Senior Analyst trong 1 nốt nhạc."
- "Làm việc của 3 người — giữ vị trí của bạn."
- "AI là intern của bạn. Bạn là sếp."

**Identity shift:** từ "người bị thay thế" → "người chỉ huy AI".

**Case study — GitHub Copilot:**
GitHub không marketing "viết code thay developer" — mà *"empower developer 55% faster"*. Kết quả: 1.3 triệu paying users trong 2 năm.

> **Fearful user mua identity, không mua features.**

---

### 2.7 Trust Hooks — Câu mở đầu xây niềm tin

| Audience | Hook example |
|---|---|
| **The Skeptic** | "Mọi người nghĩ AI sẽ giải quyết X. Dữ liệu thực tế cho thấy điều ngược lại. Đây là lý do bọn em build khác." |
| **The Overloaded** | "Bạn đang mất 2 tiếng/ngày làm việc này. Bọn em giảm xuống 10 phút — và tôi sẽ chứng minh trong 30 giây." |
| **The Fearful** | "Anh Minh, kế toán trưởng ở công ty X, dùng tool này 6 tháng. Anh đó vừa được promote. Đây là cách AI nâng tầm anh đó." |

**Common pattern xuyên suốt:**

> **Specific person + Specific number + Specific outcome.**

Mơ hồ giết niềm tin. Cụ thể tạo niềm tin.

❌ "Tăng năng suất đáng kể" — không ai tin
✅ "Anh Minh giảm 1.7 giờ/ngày" — believable

---

### 2.8 Minto Pyramid Principle — Answer First

Phương pháp giao tiếp chuẩn của McKinsey từ 1970s. Mọi consultant tier-1 đều học từ ngày đầu.

#### Bad — Bottom-up (cách kể chuyện thường)

```
1. Bối cảnh thị trường
2. Vấn đề khách hàng
3. Các giải pháp hiện có
4. Tại sao chưa đủ
5. Approach của bọn em
6. Chi tiết sản phẩm
7. Kết luận: gọi bao nhiêu vốn  ← VC không bao giờ đến đây
```

VC ngắt ở phút 2. Không bao giờ đến phần 7.

#### Good — Top-down (Minto)

```
1. ANSWER FIRST
   "Bọn em là [X], gọi $Y với traction Z"

2. 3 lý do tại sao (market / product / team)

3. Detail support nếu được hỏi
```

**Tại sao Minto work?**

Brain của human được wire theo cách *chạy đến goal trước*. Đưa kết luận trước = giảm cognitive load của người nghe.

VC nghe câu 1 → đã quyết định "nghe tiếp hay pass":
- **Nếu pass:** cảm ơn → tiết kiệm time cả 2 bên
- **Nếu interest:** họ tự đào sâu

> **Lật ngược thứ tự kể chuyện = tôn trọng time của người nghe.**

---

### 2.9 SCQA Structure — Cấu trúc mở bài

Áp dụng Minto vào câu mở bài. 4 chữ:

| Chữ | Ý nghĩa | Đặc điểm |
|---|---|---|
| **S**ituation | Bối cảnh | Ai cũng đồng ý — không tranh cãi |
| **C**omplication | Biến cố / Pain | "Nhưng vấn đề là..." |
| **Q**uestion | Câu hỏi treo | Người nghe tự tò mò |
| **A**nswer | Giải pháp | Tagline startup của bạn |

#### Ví dụ — AI cho SME e-commerce VN

**S:** "200,000 chủ shop online ở Việt Nam đang bùng nổ doanh thu trên Shopee, TikTok Shop."

**C:** "Nhưng 60% trong số họ mất 2-3 giờ/ngày trả lời cùng câu hỏi 'shop còn hàng không?' — không có thời gian bán thật."

**Q:** "Làm sao tự động 80% reply, vẫn giữ được tone cá nhân của shop?"

**A:** "ShopReplyAI — AI chatbot train trên catalog riêng từng shop trong 5 phút. Pilot 50 shop: tiết kiệm 1.7 giờ/ngày, doanh số tăng 18%. Đang gọi 500M VND seed."

**Total:** 4 câu — 30 giây pitch. Đủ để VC quyết định.

---

### 2.10 The Twitter Pitch Template

**280 ký tự bán cả startup.** Đây là test sức khỏe ý tưởng — nếu không nén được vào 280 ký tự, vấn đề không phải VC không có time. Vấn đề là bạn chưa hiểu rõ startup của chính mình.

#### Template

```
Bọn em là [Tên Startup].
Bọn em giúp [Tập khách hàng cụ thể]
giải quyết [Pain rõ ràng]
bằng [AI product, có differentiator].

Hiện đã có [Traction số cụ thể từ Day 17 PMF].
LTV/CAC = [số từ Day 18], payback [X tháng].

Đang gọi [Số tiền] để [Next milestone trong 12 tháng].
```

#### Filled example — ShopReplyAI

> Bọn em là **ShopReplyAI**. Bọn em giúp **200K chủ shop online VN** giải quyết việc **mất 2h/ngày trả tin nhắn lặp lại** bằng **AI chatbot train trên catalog riêng từng shop**. Pilot 50 shop: tiết kiệm 1.7h/ngày, doanh số +18%. LTV/CAC = 4.8x, payback 4.2 tháng. Gọi 500M VND seed để mở rộng lên 500 shop trong 6 tháng.

(Đếm thử — đúng dưới 280 ký tự.)

#### Tại sao Twitter Pitch quan trọng

1. **Cold outreach format.** DM một VC trên LinkedIn — họ chỉ đọc 2 dòng đầu. Twitter Pitch fit perfect.
2. **Test cho chính bạn.** Không nén được vào 280 ký tự = chưa hiểu rõ startup.
3. **VC sẽ paste vào Slack channel** để partners khác đọc. Pitch ngắn = dễ chia sẻ.

---

### 2.11 Tailored Pitch — Seed VC vs Series A VC

Cùng một startup. **Hai phiên bản pitch khác nhau.**

| | **Seed VC** | **Series A VC** |
|---|---|---|
| **Care về** | TAM lớn, vision 10 năm, founder-market fit | Unit Economics (LTV/CAC), growth rate, repeatable acquisition |
| **Pitch focus** | "Đây là cơ hội tỷ đô. Bọn em là người duy nhất hiểu đúng." | "Mô hình đã work. Cần vốn để scale những gì đang chứng minh được." |
| **Numbers cần** | TAM/SAM, early signals (waitlist, pilot), founder background | MRR + growth rate, LTV/CAC + Payback, cohort retention |
| **Bet vào** | Future | Present |
| **Storytelling** | Visionary | Metric-driven |

**Common mistake — gửi sai pitch cho sai người:**

| Tình huống | Hệ quả |
|---|---|
| Gửi pitch Series A cho Seed VC | Seed VC: "Startup này cần Series A, mình không invest sớm enough" → **pass** |
| Gửi pitch Seed cho Series A VC | Series A VC: "Startup này quá sớm, không có metrics" → **pass** |

**Bài học:** Trước khi gửi pitch, research VC. Họ ở giai đoạn nào? Đã invest startup nào trước? Tailor pitch theo đó.

> Bạn sẽ phải làm **2-3 versions** của Twitter Pitch — không phải 1.

---

### 2.12 Pitch Memo — Sequoia/YC format

Pitch Memo là tài liệu **nhỏ nhất** bạn có thể viết — mà thay đổi **nhiều quyết định nhất**.

#### Template — 6 sections, 1 trang A4

```
PITCH MEMO — [Tên sản phẩm]

1. THE PROBLEM (1-2 câu)
   Ai đang gặp vấn đề gì? Tần suất? Tác động kinh tế?

2. THE INSIGHT (1 câu)
   Điều mà những người khác chưa thấy / hiểu sai
   Làm gì đặc biệt khiến bạn thấy điều này?

3. THE SOLUTION (3 câu)
   - Sản phẩm làm gì?
   - Differentiator cốt lõi (so với ChatGPT, đối thủ)?
   - AI giúp như thế nào?

4. WHY NOW (1-2 câu)
   Tại sao thời điểm này — không phải 3 năm trước?
   Công nghệ / thị trường / behavior thay đổi gì?

5. TRACTION / PROOF (số cụ thể)
   - Số người dùng / pilot
   - Aha moment metric (Day 17 PMF)
   - LTV/CAC, payback (Day 18)

6. THE ASK (1-2 câu)
   Bạn cần gì? (Vốn / pilot customer / mentor / job)
   Bao nhiêu? Để làm gì trong 12 tháng tới?
```

**Tổng:** 1 trang A4. Không hơn.

#### Why this matters

> **Lưu kỹ template này — bạn sẽ dùng nó trong 10 năm tới.**

Mỗi lần đi pitch, mỗi lần raise round mới, mỗi lần tuyển C-level executive — Pitch Memo là format chuẩn.

---

## 3. Solo Pitch Lab — Hướng dẫn chi tiết

**Thời lượng:** 60 phút.
**Format:** Solo. KHÔNG ghép cặp. KHÔNG roleplay 2 người.
**Output:** 3 files trong 1 thư mục.

### 3.1 Tổng quan 5 bước

| Step | Hoạt động | Thời gian |
|---|---|---|
| **1** | Chọn audience | 5 phút |
| **2** | Viết Pitch Memo 1-pager | 15 phút |
| **3** | Viết Twitter Pitch 280 ký tự | 10 phút |
| **4** | AI VC Critique | 15 phút |
| **5** | Final revision + Self-eval | 15 phút |

---

### 3.2 Step 1 — Chọn audience (5 phút)

Quay lại reflection ở Block 1 (mini-checkpoint slide 13). Audience nào bạn đang target?

| Loại VC | Khi nào chọn |
|---|---|
| **Lead VC** (specific name) | Bạn đã research kỹ một quỹ cụ thể |
| **Seed VC** (general) | Default — phù hợp early-stage |
| **Series A VC** | Bạn đã có MRR + growth rate rõ ràng |

**Pro tip:** Nếu lừng khừng, chọn **Seed VC** — phù hợp nhất với startup early-stage.

**Output Step 1:** 1 dòng ghi rõ audience đã chọn.

---

### 3.3 Step 2 — Viết Pitch Memo 1-pager (15 phút)

Mở file `pitch_memo.md`. Copy template từ §2.12 và điền 6 sections.

#### Quy tắc viết từng section

**1. The Problem (1-2 câu)**
- ✓ Ai cụ thể đang gặp vấn đề?
- ✓ Vấn đề diễn ra với tần suất nào?
- ✓ Tác động kinh tế / vận hành?
- ❌ "Mọi người đều gặp..." (quá chung)

**2. The Insight (1 câu)**
- ✓ Điều phản trực giác — không obvious
- ✓ Bạn thấy được vì có background đặc biệt
- ❌ "Người ta cần AI tốt hơn" (mọi founder đều nói)

**3. The Solution (3 câu)**
- ✓ Câu 1: Sản phẩm làm gì
- ✓ Câu 2: Differentiator (vs ChatGPT, đối thủ)
- ✓ Câu 3: AI giúp specific như thế nào
- ❌ Liệt kê 12 features

**4. Why Now (1-2 câu)**
- ✓ Lý do timing cụ thể (cost AI giảm, behavior thay đổi, regulation mới...)
- ❌ "AI đang phát triển mạnh" (quá generic)

**5. Traction / Proof (số cụ thể)**
- ✓ Dùng số từ Day 17 PMF + Day 18 Unit Economics
- ✓ Aha moment metric cụ thể
- ❌ "Đang test với một vài shop quen biết"

**6. The Ask (1-2 câu)**
- ✓ Cần GÌ (vốn? pilot? mentor?)
- ✓ BAO NHIÊU
- ✓ Để làm GÌ trong 12 tháng
- ❌ "Bất kỳ sự hỗ trợ nào cũng được"

**Output Step 2:** File `pitch_memo.md` đầy đủ 6 sections, 1 trang A4.

---

### 3.4 Step 3 — Viết Twitter Pitch 280 ký tự (10 phút)

Mở file `twitter_pitch.md`. Cô đọng Pitch Memo về 1 đoạn.

**Cách làm:**
1. Đọc lại Pitch Memo
2. Lấy CỐT LÕI mỗi section — bỏ filler
3. Viết liền nhau thành 1 đoạn
4. Đếm ký tự (Word có Tools → Word Count, hoặc dùng [twittercharactercounter.com](https://twittercharactercounter.com))
5. Cắt cho dưới 280

**Test cuối:** Đọc to thành tiếng. Đếm time. **Phải dưới 60 giây.**

**Common mistakes:**
- Bắt đầu bằng "Em xin giới thiệu..." → cắt
- Liệt kê features → giữ 1 differentiator
- Tech jargon (RAG, vector DB...) → bỏ
- Không có ask → thêm vào cuối

**Output Step 3:** File `twitter_pitch.md` chứa:
- Twitter Pitch (dưới 280 ký tự)
- Script đọc to (45-60 giây)

---

### 3.5 Step 4 — AI VC Critique (15 phút)

Mở Claude hoặc ChatGPT. Copy prompt từ §4.1 vào.

**Quy trình:**
1. Paste full prompt vào AI
2. Paste Pitch Memo + Twitter Pitch
3. Đọc kỹ 5 critique points AI đưa ra
4. Với mỗi point, quyết định **Accept / Reject / Partial**:
   - **Accept:** AI đúng — sửa theo
   - **Reject:** AI sai — bạn biết domain hơn (ghi rõ tại sao)
   - **Partial:** Một phần đúng — sửa selective

**Cảnh báo quan trọng:**

> **AI sẽ critique bạn rất gắt. Đừng nản. Nếu AI khen bạn quá nhiều — prompt không hoạt động. Quay lại §4.1, copy đúng.**

**KHÔNG** copy AI feedback nguyên văn. AI là *critic*, bạn là *author*.

**Output Step 4:** File `ai_vc_critique_log.md` chứa:
- Pitch gốc trước critique
- Conversation với AI (full feedback)
- Quyết định Accept/Reject/Partial cho mỗi point
- Lý do với mỗi quyết định

---

### 3.6 Step 5 — Final revision + Self-eval (15 phút)

**Phần A — Revision (10 phút):**
- Sửa Pitch Memo dựa AI feedback
- Sửa Twitter Pitch dựa AI feedback
- Đọc to thành tiếng — đo time bằng đồng hồ
- Đảm bảo dưới 60 giây

**Phần B — Self-eval (5 phút):**

Pitch của bạn **pass** khi đáp ứng đủ 7 mục:

```
[ ] Mở đầu trong 8 giây gây được sự chú ý
    (số / insight phản trực giác / câu chuyện cụ thể)

[ ] Có ít nhất 1 insight phản trực giác —
    không phải câu chung mọi founder đều nói

[ ] Có ít nhất 2 con số cụ thể chứng minh —
    không phải "tăng nhiều" / "giảm đáng kể"

[ ] Differentiator rõ:
    "Tại sao OpenAI/đối thủ không làm được?"

[ ] Ask cụ thể: cần GÌ, BAO NHIÊU, để làm GÌ trong bao lâu

[ ] Đọc to dưới 60 giây (sweet spot: 45-60 giây)

[ ] Match đúng audience đã chọn ở Step 1
    (Seed = vision; Series A = metrics)
```

**Không pass đủ 7 mục → quay lại Step 4 critique tiếp.**

---

## 4. Prompts cho Vibe Coding (English-only)

> **Lưu ý:** Tất cả prompt giữ tiếng Anh 100% để AI giữ ngữ nghĩa ổn định. Thảo luận kết quả bằng tiếng Việt.

### 4.1 AI VC Critique Prompt (Prompt chính)

Dùng ở Step 4 — copy nguyên paste vào Claude/ChatGPT.

```
Act as a Partner at Sequoia Capital who has heard 50 AI startup pitches
this week. You're tired, skeptical, and have seen every variant of
"we're using LLMs to disrupt X."

Below is my 60-second pitch and Pitch Memo for an AI startup:

[paste your Pitch Memo here]

[paste your Twitter Pitch here]

Critique it ruthlessly. Answer:

1. THE 8-SECOND TEST
   Did the first sentence earn me another 50 seconds of attention?
   Why or why not? Be specific about what works/fails.

2. THE INSIGHT TEST
   What is the ONE non-obvious insight in this pitch?
   Is it actually non-obvious — or is it something every AI founder
   claims this week? If generic, suggest a sharper angle.

3. THE OPENAI THREAT
   "If OpenAI shipped this feature next week, what's your moat?"
   Force the founder to answer. If their moat is weak, point out
   exactly why.

4. THE NUMBERS TEST
   Are the traction numbers defensible? What would you push back on?
   Quote specific numbers and explain your skepticism.

5. THE WEAKEST LINE
   Quote the one sentence I would push back on hardest.
   Suggest a rewrite.

Be harsh. I'd rather hear it from you than lose a real round.
```

**Cách dùng:**
1. Paste full prompt + Pitch Memo + Twitter Pitch vào AI
2. Đọc kỹ từng critique
3. Quyết định Accept/Reject/Partial cho mỗi point
4. Sửa pitch dựa feedback
5. **KHÔNG** copy AI rewrite nguyên văn — viết lại bằng tiếng của bạn

---

### 4.2 SCQA Structure Generator

Dùng khi pitch đang yếu mở bài hoặc không có cấu trúc rõ.

```
I'm building an AI product. Help me write the SCQA opening
for my pitch.

My product context:
- Target customer: [describe]
- Pain they have: [describe]
- My solution: [describe]
- Differentiator: [describe]

Generate 3 different SCQA versions:

VERSION 1 — For Skeptic audience
S: [Situation no one disputes]
C: [Counter-intuitive complication]
Q: [Question that makes them curious]
A: [Solution with proof]

VERSION 2 — For Optimistic Seed VC
[Same SCQA structure but visionary tone]

VERSION 3 — For Pragmatic Series A VC
[Same SCQA structure but metrics-driven]

Each version should be 4 sentences max. Be specific —
no generic phrases like "leveraging AI" or "transforming X."
```

---

### 4.3 Twitter Pitch Refiner

Dùng khi Twitter Pitch quá dài hoặc chưa sắc.

```
Here's my Twitter Pitch (currently [X] characters):

"[paste your pitch here]"

It needs to be under 280 characters.

Critique it on 5 dimensions and rewrite a tighter version:

1. CHARACTER COUNT
   Current count + which sentences add length without value?

2. HOOK STRENGTH
   First 50 characters — does it grab attention?
   What number or insight could replace the opening?

3. CONCRETE vs ABSTRACT
   Identify any vague phrases ("solving X," "improving Y")
   and suggest specific replacements.

4. PROOF DENSITY
   Are the numbers concrete and verifiable?
   Or do they smell like guesses?

5. ASK CLARITY
   Is the final ask specific (amount + use of funds)?

Then provide a rewritten version under 280 characters that
keeps the soul but tightens every word.
```

---

### 4.4 Audience Tailoring Prompt

Dùng để tạo phiên bản pitch khác cho audience khác.

```
Here is my current pitch (tailored for [current audience type]):

"[paste pitch here]"

Now rewrite it for a different audience: [Seed VC / Series A VC /
Hackathon Judge / Hiring Manager — choose one].

For the new version:

1. AUDIENCE PRIORITIES
   What does this audience listen for? List top 3 things they care about.

2. LANGUAGE SHIFT
   What jargon/keywords should I use that resonates with them?
   What language should I REMOVE?

3. PROOF EMPHASIS
   What numbers/proof matter most to them?
   What can I de-emphasize?

4. ASK ADJUSTMENT
   How should the "ask" be framed differently?
   (Amount, use of funds, expected milestones)

5. REWRITE
   Provide a fully rewritten 60-second pitch tailored for them.
   Keep the core insight, but adjust framing, language, and proof.

Length: 200-280 characters for Twitter Pitch version.
```

---

### 4.5 Differentiator Sharpener (OpenAI Threat)

Dùng khi câu trả lời cho "If OpenAI did this..." còn yếu.

```
Every AI startup gets this question from VCs:
"If OpenAI / Anthropic / Google shipped this feature next week,
why would you survive?"

Here's my current answer:

"[paste your answer here]"

Critique my answer ruthlessly. Then help me sharpen it.

1. WEAKNESS IDENTIFICATION
   Is my moat actually defensible — or is it something OpenAI
   could replicate in 1 sprint? Be specific.

2. MOAT CATEGORIES
   Help me think through which type of moat I might have:
   - Data moat (unique training data)
   - Distribution moat (channel access)
   - Workflow integration moat (deeply embedded)
   - Network effects moat
   - Domain expertise moat
   - Trust/regulation moat

3. STRENGTHEN ANSWER
   Based on my product, suggest the strongest 1-2 moat categories
   I should emphasize. Provide a 2-sentence answer that defends
   my position.

4. FALLBACK RESPONSE
   If OpenAI did launch a competing feature tomorrow, what would
   I credibly do to survive? Suggest 2-3 concrete actions.

Be honest. If my moat is actually weak, tell me — better to
know now than at the partner meeting.
```

---

## 5. Checkpoints — Output yêu cầu

### 5.1 Checkpoint 1 — Stakeholder Map (cuối Block 1, 09:55)

**Output:** Trả lời 3 câu hỏi:
1. Lead VC lý tưởng (specific name)
2. Foundation Model dependency + plan B
3. Early Adopter community cụ thể (Reddit/Discord/Facebook Group)

**Pass signals:**
- Tên cụ thể, không generic
- Có evidence quỹ đó invest startup tương tự
- Plan B realistic (multi-model, fallback)
- Community thực sự tồn tại, có thể access

**Fail signals:**
- "Bất kỳ quỹ nào cũng được"
- Không biết quỹ tier-1 ở Việt Nam
- Không có plan B nếu OpenAI khóa API
- Community mơ hồ ("người dùng tiềm năng")

---

### 5.2 Checkpoint 2 — User Hook (cuối Block 2, 10:45)

**Output:** Hook 1 câu (dưới 25 từ) cho 1 archetype cụ thể (Skeptic / Overloaded / Fearful).

**Pass signals:**
- Specific person + Specific number + Specific outcome
- Đánh trúng nỗi sợ của archetype
- Cho thấy "superpower" họ nhận được
- Đọc to dưới 10 giây

**Fail signals:**
- "AI giúp bạn năng suất hơn"
- Không có tên người cụ thể
- Không có con số
- Generic — bất kỳ AI startup nào cũng dùng được

---

### 5.3 Checkpoint 3 — Self-Evaluation (Solo Pitch Lab, 12:50)

**Output:** Pitch đã pass 7 mục Self-Eval Rubric (§3.6).

**Pass signals:**
- Đủ 7 mục check
- Đã qua AI VC critique
- Có decision log rõ ràng (Accept/Reject/Partial)
- Final pitch đọc to dưới 60 giây

**Fail signals:**
- Pitch quá 90 giây hoặc dưới 30 giây
- Tech jargon từ câu đầu
- Không có proof bằng số
- Không có ask cụ thể
- Copy AI feedback nguyên văn

---

### 5.4 Final Checklist — Trước 13:00

```
[ ] 1. pitch_memo.md — 6 sections đầy đủ, 1 trang A4
[ ] 2. twitter_pitch.md — dưới 280 ký tự + script 45-60 giây
[ ] 3. ai_vc_critique_log.md:
       - Pitch gốc
       - AI feedback
       - Decision Accept/Reject/Partial
       - Pitch final đã sửa
[ ] 4. Đọc to pitch final — dưới 60 giây
[ ] 5. Tự check 7 mục Self-Eval Rubric
[ ] 6. Nén ZIP: [Tên]_Day19.zip
[ ] 7. Nộp LMS trước 13:00
```

**Minimum bar:** Nếu một Lead Partner Sequoia mở pitch của bạn lúc 9h sáng (cùng 200 deck khác), họ sẽ:
- **Đọc tiếp** sau 8 giây?
- **Hiểu** bạn làm gì sau 30 giây?
- **Quyết định follow-up** sau 60 giây?

Nếu trả lời CÓ cho cả 3 câu — pitch của bạn pass.

---

## 6. Rubric & Submission

### 6.1 Cách nộp bài

Day 19 chỉ có **1 phiên bản nộp duy nhất**:

| Mục | Yêu cầu |
|---|---|
| **Nộp khi nào** | Cuối buổi sáng Day 19 — **trước 13:00** |
| **Nộp ở đâu** | Submit trực tiếp trên LMS |
| **Tên file** | `[Tên]_Day19.zip` |
| **Bao gồm** | 3 files .md trong 1 thư mục |

> **KHÔNG có BTVN.** Day 19 hoàn tất trong buổi sáng. Tất cả công việc cần xong tại lớp.

---

### 6.2 Rubric — 100 điểm, 5 tiêu chí

| # | Tiêu chí | Điểm |
|---|---|---:|
| 1 | **Audience Targeting** | 20 |
| 2 | **Pitch Craft** | 30 |
| 3 | **Specificity & Proof** | 25 |
| 4 | **Differentiator & Defensibility** | 15 |
| 5 | **AI Critique Quality** | 10 |

---

#### Tiêu chí 1 — Audience Targeting (20 điểm)

Chấm việc bạn chọn audience đúng và pitch tailored phù hợp.

- ✓ Chọn audience cụ thể (Seed/Series A/Lead VC name)
- ✓ Ngôn ngữ match audience (Seed = vision; Series A = metrics)
- ✓ Numbers phù hợp (Seed = TAM/early signals; Series A = MRR/LTV-CAC)
- ✓ Tone & framing match expectation của audience

**Điểm cao nhất:** Pitch có thể *immediately* nhận biết là cho Seed VC vs Series A VC dựa trên ngôn ngữ.

---

#### Tiêu chí 2 — Pitch Craft (30 điểm)

Chấm cấu trúc pitch theo Minto + SCQA + 8-second test.

- ✓ Mở đầu trong 8 giây grab attention (số / insight / câu chuyện)
- ✓ Cấu trúc SCQA rõ ràng
- ✓ Answer First — không bottom-up
- ✓ Đọc to dưới 60 giây
- ✓ Pitch Memo đủ 6 sections, 1 trang A4
- ✓ Twitter Pitch dưới 280 ký tự

**Điểm cao nhất:** Pitch cảm thấy "natural" — không gồng, không jargon, kể chuyện liền mạch.

---

#### Tiêu chí 3 — Specificity & Proof (25 điểm)

Chấm độ cụ thể của các claim.

- ✓ Tên người cụ thể (champion, beta tester)
- ✓ Số liệu cụ thể từ Day 17 PMF + Day 18 Unit Economics
- ✓ Tránh từ generic ("tăng đáng kể", "rất nhiều người dùng")
- ✓ Differentiator có concrete metric (vd: "5 phút train" không phải "AI tiên tiến")
- ✓ Pain quantified (vd: "2 giờ/ngày" không phải "tốn nhiều thời gian")

**Điểm cao nhất:** Mỗi câu trong pitch đều có ít nhất 1 number, name, hoặc concrete fact.

---

#### Tiêu chí 4 — Differentiator & Defensibility (15 điểm)

Chấm khả năng defend pitch trước câu hỏi "If OpenAI did this..."

- ✓ Differentiator rõ ràng và specific
- ✓ Moat được explain (data / distribution / workflow / domain expertise)
- ✓ Có response ready cho "OpenAI threat" question
- ✓ Insight phản trực giác — không chung chung

**Điểm cao nhất:** Insight + moat strong enough để VC gật đầu sau khi nghe.

---

#### Tiêu chí 5 — AI Critique Quality (10 điểm)

Chấm chất lượng `ai_vc_critique_log.md`.

- ✓ Có conversation với AI VC đầy đủ
- ✓ Quyết định Accept/Reject/Partial cho mỗi point
- ✓ Lý do giải thích — không chỉ "có/không"
- ✓ Final pitch khác đáng kể so với pitch gốc (chứng tỏ đã iterate thực sự)

**Điểm cao nhất:** Có ít nhất 1 *Reject* hoặc *Partial* với lý do thuyết phục — cho thấy bạn không copy AI mù.

---

### 6.3 Grade bands

| Band | Điểm | Ý nghĩa |
|---|---:|---|
| Outstanding | 90–100 | Có thể đem pitch này đi gặp investor thật ngay |
| Strong | 75–89 | Cần 1-2 round refine trước khi gặp investor |
| Pass | 60–74 | Hiểu framework nhưng pitch còn tech-focused |
| Needs rework | 40–59 | Sai concept core (jargon, no numbers, no ask) |
| Fail | <40 | Chưa đạt minimum bar |

---

### 6.4 Lưu ý khi làm bài

- **Đừng copy AI feedback nguyên văn.** Mất ngay 10 điểm Tiêu chí 5.
- **Đừng dùng tech jargon** (RAG, vector DB, fine-tuning) ở câu đầu. VC không quan tâm.
- **Đừng pitch features.** Pitch outcomes.
- **Specific person + Specific number + Specific outcome** — pattern xuyên suốt.
- **Đọc to thành tiếng** trước khi nộp. Nếu nghe gồng — cần sửa.
- **Match audience.** Pitch Seed cho Series A VC = họ pass. Vice versa.

---

## 7. References

### Core readings

1. **Y Combinator — How to Pitch Your Startup**
   https://www.ycombinator.com/library/2u-how-to-build-your-seed-round-pitch-deck
   YC Partner Aaron Harris breakdown cách pitch — chuẩn cho Seed.

2. **Sequoia Capital — Writing a Business Plan**
   https://articles.sequoiacap.com/writing-a-business-plan
   Template Pitch Memo gốc của Sequoia — định nghĩa industry standard.

3. **The Pyramid Principle** — Barbara Minto
   Sách nguyên gốc về Minto Pyramid. Mọi consultant tier-1 đều đọc.

4. **DocSend — Pitch Deck Statistics**
   https://docsend.com/state-of-pitch-deck-2024
   Data về VC behavior — average time spent, slides skipped.

### Further reading (optional)

5. **The Mom Test** — Rob Fitzpatrick
   Cách phỏng vấn user để biết ai thực sự cần — không phải ai *nói* cần.

6. **Crossing the Chasm** — Geoffrey Moore
   Framework cho Early Adopters → Mainstream adoption.

7. **Build-in-Public Movement** — Pieter Levels' tweets
   https://twitter.com/levelsio
   Case study founder solo build cộng đồng + raise vốn qua Twitter.

8. **Prosci ADKAR Model**
   https://www.prosci.com/methodology/adkar
   Original framework cho change management.

### Quick reference — câu chốt Day 19

| Câu chốt |
|---|
| "Investors don't fund products. They fund **narratives**." |
| "Bạn không đua với startup khác. Bạn đua với **8 giây attention** của VC." |
| "Người dùng không thiếu tool. Họ thiếu **lý do** để thay đổi thói quen." |
| "Skeptic không sợ AI sai — họ sợ **không biết khi nào** AI sai." |
| "Fearful user mua **identity**, không mua features." |
| "**1 champion authentic > 1 triệu paid ads**." |
| "Specific person + Specific number + Specific outcome." |
| "Lật ngược thứ tự kể chuyện = tôn trọng time của người nghe." |
| "Pitch Memo là tài liệu nhỏ nhất bạn viết — thay đổi nhiều quyết định nhất." |
| "A great AI product can still die from a bad pitch." |

---

*Chúc các bạn pitch lọt tai — from product → to people → to yes.*
