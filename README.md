# Track1_Day17 — Problem Interview Practice (VLearn)

> Bài lab: reverse một **solution directive** thành problem/JTBD hypothesis, thiết kế problem interview theo The Mom Test, luyện phỏng vấn chéo và sửa Conversation Guide trước fieldwork thật.
>
> **Đây là buổi luyện tập kỹ năng, chưa phải validation.** Nhóm không tuyên bố validated sau bốn cuộc phỏng vấn.

**Thời lượng:** 2 giờ 30 phút · **Nhóm:** 4 người · **Hình thức:** mỗi thành viên phỏng vấn 1 người ngoài nhóm và nộp bản ghi của lượt mình làm interviewer.

---

## 1. Thông tin cá nhân và nhóm

| Mục          | Nội dung                    |
| ------------ | --------------------------- |
| MHV          | `2A202602585`               |
| Họ và tên    | `Phùng Gia Khánh`           |
| Tên nhóm     | `H3201`                     |
| Case đã chọn | `Case C — AI Support Radar` |

**Thành viên nhóm:**

| #   | MHV           | Họ và tên             | Vai trò trong lab   |
| --- | ------------- | --------------------- | ------------------- |
| 1   | `2A202602636` | `Bùi Hải Nam`         | Điều phối Chặng 1–2 |
| 2   | `2A202602675` | `Chử Trần Phương Nam` | Ghi chép & hợp nhất |
| 3   | `2A202602585` | `Phùng Gia Khánh`     | Phản biện guide     |
| 4   | `2A202602930` | `Phan Duy Thành`      | Bản ghi & nộp bài   |

_Vai trò là đề xuất phân công, nhóm đổi được. Ý nghĩa:_

- **Điều phối Chặng 1–2:** chủ trì buổi hội tụ draft của 4 người, chốt Problem Hypothesis, giữ Pain A và Pain B không bị gộp thành một.
- **Ghi chép & hợp nhất:** tổng hợp draft thành chuỗi Solution → Change → Actor → Situation & Job → Pain; tách rõ _user nói gì_ và _nhóm diễn giải gì_.
- **Phản biện guide:** giữ vai hoài nghi — soát xem có câu nào làm lộ solution và chịu trách nhiệm câu hỏi "đáng sợ" ở Big 3 #1.
- **Bản ghi & nộp bài:** nhắc xin consent trước khi ghi, thu bản ghi của cả nhóm, chạy checklist §6 trước khi nộp.

**Người mình đã phỏng vấn:** `Lê Thanh Tình` (ngoài nhóm) · **Ngày phỏng vấn:** `10/03/2026, 9:00 AM`

---

## 2. Problem Hypothesis Brief

_Kết quả Chặng 1 của nhóm. Toàn bộ nội dung trong phần này là **hypothesis**, chưa phải fact về user._

> ⚠️ Bản dưới đây do AI hỗ trợ diễn đạt ở bước đầu (khai báo ở §5). Đây **chưa phải** kết luận của nhóm: mỗi thành viên phải tự đọc lại, đối chiếu với cách hiểu riêng của mình và sửa trực tiếp vào đây trước khi dùng để phỏng vấn.

Chuỗi suy luận nhóm đi theo:

```
Solution → Change → Actor → Situation & Job → Pain → Evidence
```

### 2.1. Solution → Capability trung tính

**Solution directive (nguyên văn):**

```text
Sau mỗi phiên học, hệ thống phân tích các tín hiệu như di chuyển giữa slide, dừng lâu hoặc xem lại,
highlight và ghi chú, đánh dấu "Chưa hiểu", thay đổi câu trả lời, và nội dung trao đổi với AI Chat.
AI tạo một Support Queue cho giảng viên, gồm: (1) những học viên có thể cần hỗ trợ, (2) phần nội dung
mà họ có thể đang gặp khó khăn, (3) các tín hiệu dẫn đến nhận định đó, (4) một hành động hỗ trợ được
đề xuất. Giảng viên xem lại và quyết định có liên hệ với học viên hay không.
```

**Các thành phần directive đã mô tả:**

| Thành phần    | Directive đã mô tả                           |
| ------------- | -------------------------------------------- |
| Trigger       | Kết thúc một phiên học                       |
| Input         | Slide navigation, notes, answers, AI Chat    |
| AI action     | Suy đoán nhu cầu hỗ trợ và xếp mức ưu tiên   |
| Output        | Support Queue cho giảng viên                 |
| Human control | Giảng viên quyết định có can thiệp hay không |

**Capability trung tính (bỏ tên feature, màn hình, công nghệ):**

```text
Phát hiện sớm rằng một learner đang mắc ở một phần nội dung cụ thể trong lúc tự học — dựa trên dấu vết
hành vi học tập của họ — và chuyển phát hiện đó thành một việc cần làm rõ ràng cho người có khả năng
hỗ trợ, để learner được giúp trước khi việc học đổ vỡ.
```

**Nhóm có đang mặc định cách triển khai được giao là cách duy nhất không?**

Có. "Support Queue cho giảng viên" chỉ là **một** cách triển khai. Capability ở trên còn có thể đáp ứng bằng các hướng khác (xem Solution Parking Lot ở §2.7) — trong đó có hướng không dùng AI. Đây là điều phải kiểm tra bằng evidence, không được coi là hiển nhiên.

### 2.2. Change — chuỗi thay đổi được kỳ vọng

```
Solution → Người hỗ trợ biết ai đang kẹt ở đâu → Người hỗ trợ can thiệp sớm → Learner gỡ được chỗ vướng
```

| #   | Thay đổi được kỳ vọng                                                                     | Là output của team hay outcome team chỉ có thể ảnh hưởng? |
| --- | ----------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 1   | Người hỗ trợ (coach/instructor) **nhìn thấy** được ai đang kẹt và kẹt ở phần nội dung nào | Output của team — team làm ra được thứ này                |
| 2   | Người hỗ trợ **đổi hành vi**: chủ động liên hệ/điều chỉnh trước khi learner tự bỏ qua     | Hành vi của người khác — team chỉ có thể ảnh hưởng        |
| 3   | Learner **chấp nhận** hỗ trợ và gỡ được chỗ vướng, không bỏ qua phần nội dung đó          | Hành vi của learner — team chỉ có thể ảnh hưởng           |

**Outcome kỳ vọng:** giảm lỗ hổng kiến thức tích lũy và tăng mức hoàn thành/gắn kết với khóa học.

**Nếu learner (hoặc người hỗ trợ) không đổi hành vi thì solution có tạo được outcome không?**

Không. Solution chỉ tạo ra **visibility**. Nếu người hỗ trợ không hành động, hoặc learner không đón nhận hỗ trợ, thì mọi thứ dừng ở mắt xích 1 và không có outcome nào. Đây là giả định yếu nhất trong chuỗi và phải được kiểm tra bằng evidence.

### 2.3. Actor — các nhóm người liên quan

| Actor                                                      | Họ đang làm gì?                                                                                  | Pain hoặc hậu quả có thể có                                                                                                            | Họ hưởng lợi thế nào?                                                                |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| **Learner** (người trực tiếp tạo ra tín hiệu học tập)      | Tự học slide/bài một mình, làm quiz, ghi chú; khi không hiểu thì tự xoay hoặc bỏ qua để học tiếp | Bị mắc nhưng không ai biết; tự xử tốn thời gian; bỏ qua phần khó → nợ kiến thức tích lũy, mất đà học                                   | Được hỗ trợ đúng chỗ, đúng lúc, ngay trong lúc còn đang học                          |
| **Coach / Mentor**                                         | Đồng hành learner theo nhóm hoặc 1-1; chỉ nhận được thông tin khi learner chủ động lên tiếng     | Chỉ biết learner kẹt khi được hỏi; hỗ trợ muộn và lệch chỗ; thời gian bị dồn vào người lên tiếng to nhất chứ không phải người cần nhất | Biết được nên dành thời gian cho ai, ở nội dung nào                                  |
| **Instructor / TA** (người nhận Support Queue)             | Dạy, soạn nội dung, xử lý câu hỏi của lớp; đánh giá mức hiểu bài chủ yếu qua bài kiểm tra        | Không có cách thấy được ai đang tụt giữa các buổi; chỉ phát hiện khi đã muộn (điểm thấp/learner biến mất)                              | Can thiệp sớm, phân bổ thời gian hỗ trợ đúng người, chỉnh được cả nội dung bài giảng |
| **Bạn học / peer** (nguồn hỗ trợ nhanh nhất trong thực tế) | Được hỏi trực tiếp qua chat/nhóm lớp khi learner không hiểu                                      | Bị hỏi những câu lặp lại; trả lời sai hoặc qua loa                                                                                     | Nắm nội dung tốt hơn khi phải giải thích lại                                         |

**Actor nhóm chọn để điều tra trước:** **Learner** (người đang tự học trên VLearn)

**Vì sao chọn nhánh này thay vì actor khác:**

1. Learner là người **trực tiếp trải nghiệm barrier** — nếu họ không thực sự mắc kẹt lâu và âm thầm, thì cả chuỗi change phía sau (queue → instructor can thiệp) mất chân đế.
2. Hành vi của learner là **điều kiện tiên quyết** để mắt xích 2 và 3 xảy ra (họ phải đón nhận hỗ trợ). Nếu learner phản đối việc bị "gắn cờ", solution phản tác dụng — giả thuyết này chỉ kiểm tra được bằng lời kể của learner.
3. **Giới hạn của vòng này:** cả 4 thành viên phỏng vấn learner, nên phía coach/instructor (mắt xích 2) **không** được kiểm chứng. Đây là giới hạn nhóm tự khai báo, không phải kết luận về job của instructor.

### 2.4. Situation & Job

```
Tình huống bắt đầu
→ User muốn hoàn thành việc gì
→ Hiện tại họ làm như thế nào
→ Điểm bắt đầu gặp vướng mắc
```

**Situation & Job:**

Khi **đang tự học một bài/slide khó trên VLearn vào buổi tối, một mình, không có ai ngồi cạnh**, **learner** đang cố **hiểu đủ nội dung để học tiếp và làm bài tập/quiz đúng hạn** bằng cách **tua lại slide, đọc lại từ đầu, tra Google/YouTube, copy câu hỏi vào AI Chat, hoặc hỏi bạn học trong nhóm lớp**.

**Điểm bắt đầu gặp vướng mắc:** learner không xác định được mình đang thiếu **khái niệm nền nào** để hỏi cho đúng; và kênh hỏi chính thức (mentor/TA) thì chậm (chờ trả lời) hoặc đáng ngại (phải thừa nhận mình không hiểu).

**JTBD Hypothesis:**

Khi **bị mắc ở một phần nội dung trong lúc tự học một mình**, tôi muốn **gỡ được chỗ vướng ngay trong lúc còn đang học**, để có thể **học tiếp bình thường mà không bị dồn nợ kiến thức về sau**.

_Ghi chú: Job này vẫn tồn tại nguyên vẹn nếu bỏ toàn bộ AI, Support Queue và feature ra khỏi bối cảnh._

### 2.5. Pain Hypothesis — hai cách giải thích cạnh tranh

**Pain Hypothesis A (visibility gap):**

Khi **tự học một phần nội dung khó trên VLearn**, **learner** gặp khó khăn trong việc **gỡ chỗ vướng để học tiếp** vì **không có ai ở vai trò hỗ trợ biết được họ đang mắc ở đâu (và bản thân họ cũng không chủ động lên tiếng)**, dẫn đến **việc họ tự xoay bằng workaround tốn thời gian hoặc bỏ qua phần đó, khiến lỗ hổng kiến thức tích lũy và đà học giảm dần**.

**Pain Hypothesis B (cách giải thích cạnh tranh):**

Khi **tự học một phần nội dung khó trên VLearn**, **learner** gặp khó khăn trong việc **gỡ chỗ vướng** vì **việc đi hỏi có chi phí xã hội và thời gian quá cao (ngại bị đánh giá là không tự tìm hiểu, hỏi xong phải chờ, không biết hỏi ai cho đúng)**, dẫn đến **họ chọn im lặng và tự xử dù đã biết mình đang mắc — tức vấn đề không nằm ở phát hiện mà nằm ở chính hành vi lên tiếng**.

**Giả thuyết nhóm chọn để điều tra trước:** A

**Lý do chọn và điều còn phải phân biệt:**

Nhóm chọn A vì A là **giả định nền** của cả solution directive: nếu barrier thật không phải "không ai biết" mà là "learner cố tình không nói" (B), thì việc phát hiện tự động **không** giải quyết được gì — thậm chí có thể làm learner khó chịu vì bị theo dõi.

Vì vậy hai giả thuyết **không loại trừ nhau**. Phỏng vấn phải tìm được cả hai loại evidence: (a) có lần nào learner mắc mà **không ai biết** và không được giúp; (b) có lần nào learner **biết cách hỏi nhưng vẫn không hỏi**. Nếu (b) xuất hiện nhiều và mạnh hơn (a) thì nhóm phải chuyển hướng điều tra.

### 2.6. Evidence Map

| Cần kiểm tra                                                                 | Evidence làm nhóm tin hơn                                                                                                                       | Evidence làm nhóm nghi ngờ hoặc bác bỏ                                                                                       |
| ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| Situation có thật                                                            | Learner kể được **một lần cụ thể trong 7 ngày gần đây**: học bài/slide nào, tối nào, dừng ở đoạn nào                                            | Không nhớ được lần nào; chỉ nói được "thường thì mình hay bị" mà không có chi tiết nào                                       |
| Pain có ý nghĩa                                                              | Việc mắc kéo dài nhiều phút → nhiều giờ; learner nói được cảm giác lúc đó ("bực", "mất đà", "hoang mang") và nó ảnh hưởng tới việc nộp bài/điểm | Kể ra nhưng xử lý trong vài phút, thấy bình thường, không nhớ ra hậu quả nào                                                 |
| Workaround tồn tại                                                           | Có chuỗi hành động cụ thể (tua lại mấy lần, search từ khoá gì, hỏi ai, copy vào AI Chat) và **lặp lại nhiều lần**                               | Không có workaround nào — vì không cần phải xử lý                                                                            |
| Consequence tồn tại                                                          | Bỏ qua phần đó và học tiếp; làm sai quiz; phải học lại từ đầu; trễ deadline; mất động lực vài ngày                                              | Không có hậu quả quan sát được nào; mọi thứ vẫn ổn                                                                           |
| Pattern có lặp                                                               | Chuyện này xảy ra hằng tuần; learner còn kể được lần trước đó nữa                                                                               | Chỉ là sự kiện duy nhất, do hoàn cảnh đặc biệt (mất mạng, thiếu slide)                                                       |
| **Learner có muốn người khác biết mình đang kẹt không** _(phân biệt A vs B)_ | Có lần learner **muốn được hỏi thăm nhưng không biết hỏi ai**; hoặc kể chuyện được mentor chủ động hỏi trước và thấy tích cực                   | Learner nói rõ không muốn bị theo dõi/chú ý; hoặc mọi lần kẹt đều là do họ **chủ động chọn** không hỏi dù kênh hỗ trợ sẵn có |

### 2.7. Chốt Problem Hypothesis và park solution

**Problem Hypothesis nhóm mang sang Chặng 2:**

```text
Khi tự học một phần nội dung khó trên VLearn một mình, learner thường mắc lại khá lâu nhưng xử lý
âm thầm — bằng workaround tốn thời gian hoặc bỏ qua phần đó — vì không ai ở vai trò hỗ trợ biết được
họ đang mắc ở đâu, và bản thân họ cũng không chủ động lên tiếng. Hậu quả là lỗ hổng kiến thức tích
lũy và đà học giảm dần.
```

**Điều gì phải đúng để giả thuyết đứng vững:**

```text
(1) Sự kiện "mắc khi tự học" lặp lại trong tuần gần đây, learner nhớ được chi tiết.
(2) Workaround/hậu quả đủ lớn để learner kể được, không chỉ là bất tiện vài phút.
(3) Learner có mong muốn được hỗ trợ sớm hơn, và KHÔNG phản đối việc bị phát hiện/chú ý.
(4) "Không ai biết mình đang mắc" là barrier thật, không phải chỉ là cách nói lại của việc lười học.
```

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

```text
- Learner thấy mắc là chuyện bình thường, tự xử trong vài phút, không nhớ nổi lần nào → pain không đáng giải.
- Learner hỏi rất dễ dàng và được trả lời nhanh → kênh hỗ trợ đã đủ tốt, barrier "không ai biết" không tồn tại.
- Learner phản đối việc bị theo dõi/gắn cờ là người cần hỗ trợ → hướng "phát hiện rồi đưa cho instructor" phản tác dụng.
- Pain thật là thiếu thời gian / deadline chứ không phải không hiểu bài → đổi hẳn actor và situation.
- Learner biết mình mắc, biết cách hỏi, nhưng chủ động chọn không hỏi (giả thuyết B mạnh hơn A).
```

**Solution Parking Lot** _(≥ 5 hướng, trong đó ≥ 1 hướng không sử dụng AI):_

| #   | Hướng giải quyết có thể có                                                                                                                                                    | AI / Không sử dụng AI |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| 1   | **FAQ theo slide** do TA tổng hợp từ câu hỏi thật của các khóa trước, gắn ngay dưới slide                                                                                     | Không sử dụng AI      |
| 2   | **Checklist tự kiểm tra cuối bài** ("bạn có giải thích được khái niệm X bằng lời của mình không?") kèm đáp án nền ngắn                                                        | Không sử dụng AI      |
| 3   | **Peer pod hằng tuần**: 4–5 learner học cùng, có điều phối viên và một khung giờ cố định để hỏi nhau                                                                          | Không sử dụng AI      |
| 4   | **Mentor chủ động nhắn 1 câu hỏi mở** cho từng learner sau mỗi buổi ("chỗ nào hôm nay khó nhất?") — làm thủ công                                                              | Không sử dụng AI      |
| 5   | **Digest theo slide, không theo người**: thống kê tín hiệu đơn giản (slide bị xem lại nhiều nhất, tỉ lệ đổi đáp án) gửi mentor — cảnh báo nội dung khó, không gắn cờ học viên | AI                    |
| 6   | **Support Queue đúng như directive**: AI suy đoán từng learner đang kẹt ở đâu và xếp mức ưu tiên cho giảng viên                                                               | AI                    |

> **CHECKPOINT 1:** qua checkpoint khi lần theo được đủ chuỗi Solution → Change → Actor → Situation & Job → Pain → Evidence; có hai cách giải thích cạnh tranh; và nói rõ điều gì có thể làm giả thuyết được chọn trở nên sai.

---

## 3. Conversation Guide

_Bản dưới đây là bản dùng để **luyện ở Chặng 3**. Sau khi luyện, nhóm sửa lại và ghi thay đổi vào §3.8 — bản đã sửa đó mới là phiên bản cuối để nộp._

### 3.1. Tiêu chí tuyển người

Chúng tôi cần nói chuyện với người đã **tự học một bài trên VLearn (hoặc một nền tảng học online khác) và bị mắc lại ở một phần nội dung, phải dừng lại để tìm cách xử lý** trong vòng **7** ngày gần đây.

**Bốn người được phỏng vấn là bốn learner khác nhau, đều ngoài nhóm.** Không dùng câu trả lời của thành viên trong nhóm làm evidence.

> ⚠️ **Giới hạn của vòng này:** cả 4 lượt đều phỏng vấn learner → *"Vòng này chỉ có learner-side evidence; instructor-side job chưa được kiểm chứng."* Mọi kết luận về việc instructor sẽ làm gì với Support Queue đều **không** có bằng chứng trong bài này.

**Recruitment check** _(dùng để tuyển đúng người, không tính là evidence chính):_

```text
"Trong 7 ngày qua, có lần nào bạn đang học mà gặp một chỗ không hiểu, phải dừng lại xử lý không?
Chỗ đó là gì, và bạn xử lý thế nào?"
```

Nếu người đó không kể được một sự kiện cụ thể nào → không đạt tiêu chí tuyển, báo giảng viên để đổi cặp.

### 3.2. Lời mở đầu

_Nói mục đích học hỏi, không nhắc solution, không xin feedback về tính năng._

```text
"Mình là [tên], học viên khóa này. Nhóm mình đang tìm hiểu cách học viên tự học và xử lý chỗ khó
trong khóa — nên hôm nay mình chỉ muốn nghe câu chuyện thật của bạn, không giới thiệu hay đánh giá
sản phẩm gì cả. Mình xin phép ghi âm buổi nói chuyện nhé: bản ghi chỉ dùng cho bài học của nhóm mình,
không chia sẻ công khai, và bạn có thể dừng lại bất cứ lúc nào hoặc bỏ qua câu nào bạn không muốn trả lời.
Mình dự kiến hỏi khoảng 15 phút. Bạn đồng ý cho mình ghi âm chứ?"
```

Chỉ bắt đầu ghi âm **sau khi** người được phỏng vấn đồng ý.

### 3.3. Big 3 — ba điều quan trọng nhất cần học

| #   | Điều cần học                                                                                                    | Evidence cần tìm                                                                                                       | Điều gì khiến nhóm xem lại giả thuyết?                                                                                              |
| --- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| 1   | 🔥 **(câu hỏi đáng sợ)** Learner có thực sự mắc lại lâu và có thấy đó là chuyện đáng giải không?                 | Một sự kiện cụ thể trong 7 ngày: học bài nào, đoạn nào, mất bao lâu, cảm giác lúc đó, kết quả cuối cùng                | Learner nói mắc là chuyện bình thường, tự xử trong vài phút, không nhớ nổi lần nào → pain không đáng giải                           |
| 2   | Khi bị mắc, learner đã thực sự làm gì (workaround), và chi phí thật là bao nhiêu?                               | Chuỗi hành động cụ thể: tua lại mấy lần, search gì, copy vào AI Chat, hỏi ai, mất bao nhiêu thời gian, có bỏ qua không | Không có workaround nào (kẹt thì bỏ luôn, không ảnh hưởng gì) hoặc workaround rất rẻ → consequence không tồn tại                    |
| 3   | Điều gì khiến learner **không** chủ động nhờ người hỗ trợ — và họ thấy thế nào khi có ai đó chủ động hỏi trước? | Lần gần nhất learner hỏi mentor/TA/bạn học; hoặc lần định hỏi nhưng không; lần được ai đó phát hiện và nhắn trước      | Learner hỏi rất dễ dàng và được trả lời nhanh → barrier "không ai biết" không tồn tại; hoặc learner phản đối mạnh việc bị phát hiện |

_Ít nhất một điều phải là câu hỏi "đáng sợ" — câu trả lời có thể làm nhóm thay đổi hướng._

### 3.4. Story opener

> Kể mình nghe về **lần gần nhất** bạn đang học một bài mà gặp một chỗ không hiểu — bắt đầu từ lúc bạn mở bài đó?

### 3.5. Big 3 Questions

| #   | Điều cần học                                                    | Câu hỏi sẽ dùng                                                                                                                                                                                                                                                                                                               |
| --- | --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Learner có thực sự mắc lại lâu và thấy đáng giải                | "Kể mình nghe về lần gần nhất bạn học một bài mà có chỗ không hiểu — hôm đó là hôm nào? Bạn đang học bài gì, và chuyện diễn ra thế nào từ lúc mở bài tới lúc bạn dừng lại?"                                                                                                                                                   |
| 2   | Workaround và chi phí thật                                      | "Lúc nhận ra mình không hiểu chỗ đó, bạn đã làm gì tiếp theo? Cụ thể: bạn mở cái gì, tua lại chỗ nào, gõ gì để tìm, hỏi ai? Việc đó mất bao lâu? Cuối cùng bạn có hiểu được chỗ đó không, hay để lại?"                                                                                                                        |
| 3   | Điều gì chặn việc lên tiếng, và phản ứng khi bị phát hiện trước | "Lần gần nhất bạn chủ động nhờ ai đó (mentor, TA, bạn học) về một chỗ không hiểu là khi nào? Bạn hỏi ai, qua đâu, và sau đó chuyện gì xảy ra?" → rồi: "Có lần nào bạn định hỏi nhưng lại thôi không? Lúc đó vì sao?" → rồi: "Đã bao giờ có ai chủ động nhắn trước và hỏi bạn đang mắc chỗ nào chưa? Lúc đó bạn thấy thế nào?" |

### 3.6. Probe bank — chỉ dùng khi cần đào sâu câu chuyện

- "Lúc đó chuyện gì xảy ra tiếp theo?"
- "Bạn đã làm gì?"
- "Vì sao bạn chọn cách đó?"
- "Phần nào khó nhất?"
- "Bạn đã thử cách nào khác chưa?"
- "Việc đó kéo theo hậu quả gì?"
- "Lần gần nhất trước đó là khi nào?"

**Probe riêng cho Case C** _(chỉ dùng khi câu chuyện đã mở, tuyệt đối không nhắc tới việc "hệ thống phát hiện")_:

- "Chỗ đó bạn bỏ qua luôn để học tiếp, hay để lại xử lý sau? Sau đó bạn có quay lại không?"
- "Sau khi bỏ qua, việc học tiếp của bạn có bị ảnh hưởng gì không?"
- "Đã có ai chủ động nhắn trước hỏi bạn đang mắc chỗ nào chưa? Lúc đó bạn thấy thế nào?"
- "Có ai trong lớp biết bạn đang mắc chỗ đó không? Vì sao?"

**Câu hỏi KHÔNG được dùng trong buổi này** _(làm lộ solution hoặc hỏi ý kiến/dự đoán tương lai)_:

- ❌ "Nếu giảng viên biết bạn đang mắc chỗ nào thì bạn thấy thế nào?"
- ❌ "Bạn có muốn có tính năng tự phát hiện ai đang cần hỗ trợ không?"
- ❌ "Bạn có thấy Support Queue hữu ích không?"
- ❌ "Thường thì bạn có hay hỏi mentor không?" → thay bằng: "Lần gần nhất bạn hỏi mentor là khi nào?"

### 3.7. Ba phản xạ khi data bắt đầu lệch

| User đưa ra                            | Phản xạ     | Cách quay lại evidence                                     |
| -------------------------------------- | ----------- | ---------------------------------------------------------- |
| Lời khen                               | **Deflect** | Cảm ơn ngắn rồi quay lại việc họ đang làm hiện tại         |
| Câu chung chung hoặc lời hứa tương lai | **Anchor**  | "Lần gần nhất chuyện đó xảy ra là khi nào?"                |
| Ý tưởng hoặc feature request           | **Dig**     | "Điều đó giúp bạn làm được gì? Hiện tại bạn xử lý ra sao?" |

### 3.8. Những gì đã sửa so với bản nháp Chặng 2

_Điền ở Chặng 4, sau khi cả nhóm đã nghe lại bản ghi. Nếu bảng này không thay đổi gì thì guide chưa thực sự được sửa — dấu hiệu chưa đạt gate 4._

| #   | Sửa gì                                                                                                                                                                            | Vì sao (tín hiệu từ lượt luyện)                                                                                                                                              |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Story Opener phải hỏi kèm vị trí cụ thể ngay trong câu mở: "lần gần nhất bạn học bài nào, đang ở slide/đoạn nào?" thay vì chỉ neo vào "lần gần nhất" rồi mới hỏi vị trí ở câu sau | Lượt luyện của `Phan Duy Thành` → `Lê Thanh Tình` chỉ lấy được mốc thời gian ("chiều hôm qua"); user không nêu được tên bài/slide nên Situation chưa đạt mức evidence ở §2.6 |
| 2   | Sau mỗi tín hiệu khựng lại, bắt buộc hỏi ngay chuỗi hành động và thời lượng ("sau đó bạn làm gì?", "mất bao lâu?", "cuối cùng có hiểu không hay để lại?") trước khi chuyển câu    | Lượt luyện ghi nhận chỗ khựng ("thuật ngữ tiếng anh", "không biết trang slide để tìm luôn") nhưng không đào tiếp nên không có workaround, thời lượng và hậu quả              |
| 3   | Đưa nhóm câu phân biệt Pain A vs Pain B ("lần gần nhất bạn định hỏi ai nhưng lại thôi") thành câu bắt buộc, không cắt khi gần hết 15 phút                                         | Lượt luyện không ghi nhận được dữ liệu nào cho Pain B, nên không phân biệt được A với B                                                                                      |

### 3.9. Tự rà soát guide trước khi phỏng vấn

- [ ] Không có câu nào làm lộ solution (không nhắc "AI", "Support Queue", chuyện giảng viên phát hiện learner, không mô tả tính năng).
- [ ] Không có câu nào hỏi ý kiến hoặc dự đoán tương lai ("bạn có muốn", "bạn có hay", "nếu có thì bạn thấy sao").
- [ ] Story opener đã neo vào "lần gần nhất".
- [ ] Ba câu hỏi chính nối trực tiếp với Big 3.
- [ ] Có ít nhất một câu đủ sức làm giả thuyết yếu đi (Big 3 #1 và #3).
- [ ] Người được phỏng vấn đã đáp ứng tiêu chí tuyển (đã qua recruitment check).
- [ ] Mỗi thành viên đã biết mình sẽ phỏng vấn ai.

### 3.10. Phân công phỏng vấn

| Thành viên                          | Phỏng vấn ai (learner ngoài nhóm) | Thời gian | Đã xin phép ghi âm |
| ----------------------------------- | --------------------------------- | --------- | ------------------ |
| `Bùi Hải Nam` (2A202602636)         | `Vũ Quang Tiến` (2A202602872)     | 15p       | có                 |
| `Chử Trần Phương Nam` (2A202602675) | `Chu Thuỳ Dương` (2A202602660)    | ~5–7 phút | `Có`               |
| `Phùng Gia Khánh` (2A202602585)     | `Lê Anh Duy` (2A202602723)        | 15p       | có                 |
| `Phan Duy Thành` (2A202602930)      | `Lê Thanh Tình`                   | 15 phút   | `Có`               |

> Mỗi người tự ghi lại **đúng lượt mình làm interviewer** vào `interview/notes.md`.

> **CHECKPOINT 2:** guide đạt nếu bắt đầu từ một sự kiện gần đây; ba câu hỏi chính nối trực tiếp với Big 3; probe bank có thể đào hành vi–workaround–hậu quả; và không để lộ solution directive.

---

## 4. Practice Reflection

_Mỗi thành viên tự hoàn thành phần này sau khi nghe lại bản ghi của chính mình._

**1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?**

```text
Story Opener neo vào "lần gần nhất" đã mở được chuyện: user nêu được mốc thời gian ("chiều hôm qua").
Câu hỏi về điều gì khiến bị khựng lại lấy được loại tín hiệu cụ thể ("gặp những thuật ngữ tiếng anh"),
và câu hỏi về cảm xúc đầu tiên lấy được trạng thái lúc đó ("buồn", "lo lắng").
```

**2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**

```text
Chưa đào tiếp sau tín hiệu khựng lại: khi user nói "không biết trang slide để tìm luôn" và gặp thuật
ngữ tiếng Anh, mình không hỏi ngay "sau đó bạn làm gì?" nên mất phần workaround, thời lượng mắc kẹt
và hậu quả — đây là chỗ quyết định evidence cho Big 3 #2. Câu hỏi về vị trí (bài/slide nào) vẫn còn
quá chung, user trả lời được nhưng không neo vào nội dung cụ thể.
```

**3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**

```text
Ba sửa đổi ghi ở §3.8: (1) gộp câu hỏi vị trí cụ thể vào ngay Story Opener để Situation có chi tiết;
(2) bắt buộc hỏi chuỗi hành động + thời lượng ngay sau mỗi tín hiệu khựng lại để lấy workaround và
hậu quả; (3) đưa câu phân biệt Pain A vs Pain B thành câu bắt buộc vì lượt luyện không chạm tới.
```

---

## 5. AI Support Log

_Mọi cách dùng AI phải được khai báo. AI **không** được dùng để tạo interview data, bịa quote, suy diễn chi tiết user chưa nói hoặc viết reflection thay cho việc tự nghe lại cuộc phỏng vấn._

| #   | Dùng AI ở đâu (chặng / bước)                                            | AI đã giúp gì                                                                                                                                                      | Điểm sai hoặc hời hợt của AI                                                                                                                                      | Mình đã tự sửa thế nào                                                                                                                                                              |
| --- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Chặng 1 — dựng chuỗi Solution → Change → Actor → Situation & Job → Pain | AI (Copilot) gợi ý cấu trúc chuỗi suy luận, giúp tách capability trung tính khỏi tên feature và nhắc thêm một giả thuyết cạnh tranh (chi phí xã hội khi lên tiếng) | AI viết pain nghe rất hợp lý nhưng có xu hướng trôi về phía "thiếu công cụ phát hiện" — tức solution đội lốt problem; AI cũng trình bày như thể đã chắc chắn đúng | Nhóm viết lại pain theo dạng barrier + consequence, tách rõ phần nào là hypothesis; giữ luôn cả Pain B để buộc phải phân biệt bằng evidence; coi toàn bộ §2 là draft phải tự review |
| 2   | Chặng 2 — soạn Conversation Guide                                       | AI gợi ý cách diễn đạt câu hỏi theo dạng "lần gần nhất…", giúp biến Big 3 thành câu hỏi bám hành vi quá khứ và soát lại các câu dễ dẫn dắt                         | AI đưa ra vài câu hỏi vẫn còn mời user đánh giá solution (kiểu "nếu giảng viên biết thì bạn thấy sao") và vài câu hỏi "thường thì…"                               | Nhóm đưa các câu đó vào danh sách "Câu hỏi KHÔNG được dùng"; thay bằng câu neo vào sự kiện đã xảy ra                                                                                |
| 3   | Chặng 2 và chuẩn bị nộp bài — rà soát guide, dựng checklist             | AI đối chiếu README với 4 gate, chỉ ra phần còn thiếu và gợi ý checklist tự rà soát guide (§3.9)                                                                   | AI viết ra checklist nghe rất đầy đủ nhưng dễ khiến nhóm tick cho xong mà không thật sự soi lại từng câu hỏi; AI cũng sẵn sàng viết luôn phần reflection          | Nhóm tự đọc lại guide theo từng mục §3.9; §4 Practice Reflection để từng người tự viết sau khi nghe lại bản ghi của mình, không dùng AI                                             |

**Kết luận về mức độ tin cậy của phần có AI hỗ trợ:**

```text
AI chỉ được dùng để gợi ý cách diễn đạt và soát câu hỏi dẫn dắt. AI KHÔNG được dùng để tạo interview
data, bịa quote, suy diễn chi tiết user chưa nói, hoặc viết Practice Reflection thay cho việc tự nghe
lại bản ghi. Mọi nội dung trong §2 và §3 là giả thuyết do nhóm tự rà lại và tự chịu trách nhiệm —
chưa có dòng nào trong đó được coi là evidence về user.
```

---

## 6. Nộp bài

### Cấu trúc repo

```text
Track1_Day17_MHV_HoVaTen/
├── README.md
└── interview/
    ├── notes.md
    └── recording.m4a       # hoặc recording.mp3 / recording.mp4
```

Nếu bản ghi lưu trên Drive hoặc nền tảng gọi trực tuyến, thay file audio/video bằng `interview/recording-link.md`. Link phải mở được với giảng viên/TA và **không** để chế độ công khai.

> _Repo hiện tại là repo nhóm: `thanhpd123/Day17-Track1-H3201`. Nếu giảng viên yêu cầu đúng tên `Track1_Day17_<MHV>_<HoTen>` thì tạo repo cá nhân riêng cho phần nộp và giữ repo này làm bản dùng chung của nhóm._

`interview/notes.md` chứa Interview Record của **chính lượt bạn làm interviewer**. Không bắt buộc nộp transcript; bản ghi được giữ lại để có thể bóc transcript và review sau.

### Checklist trước khi nộp

- [ ] Repo đúng tên `Track1_Day17_MHV_HoVaTen`.
- [ ] `README.md` đủ năm phần.
- [ ] `interview/notes.md` là notes của chính lượt bạn làm interviewer.
- [ ] Bản ghi hoặc recording link mở được với giảng viên/TA.
- [ ] Người được phỏng vấn đã đồng ý cho ghi lại.
- [ ] Conversation Guide không làm lộ solution và đã được sửa sau khi luyện.

### Bốn gate đánh giá

| Gate                     | Đạt khi                                                                | Dấu hiệu chưa đạt                                              |
| ------------------------ | ---------------------------------------------------------------------- | -------------------------------------------------------------- |
| 1. Problem Framing       | Đi đủ chuỗi Solution → Evidence; giả thuyết cụ thể và có thể bị bác bỏ | Pain chứa tên feature; actor hoặc situation chung chung        |
| 2. Interview Design      | Big 3 nối với điều cần học; guide hỏi quá khứ và không làm lộ solution | Hỏi "bạn có muốn/dùng không"; câu hỏi không gắn với hypothesis |
| 3. Interview Practice    | Có bản ghi được consent; interviewer follow câu chuyện và đào hành vi  | Đọc bảng hỏi máy móc; nói nhiều; pitch solution                |
| 4. Reflection & Revision | Chỉ ra lỗi cụ thể và sửa Conversation Guide dựa trên trải nghiệm luyện | Reflection chung chung; guide sau luyện không thay đổi         |

---

## Phụ lục — Luật của bài lab

1. **Không cho interviewee xem solution directive.** Đây là problem interview, không phải concept interview.
2. **Hỏi về quá khứ cụ thể.** Ưu tiên "lần gần nhất" hơn "thường thì" hoặc "bạn có muốn".
3. **Mỗi người phỏng vấn một người ngoài nhóm.** Không dùng câu trả lời của thành viên cùng nhóm làm evidence.
4. **Ghi facts trước, diễn giải sau.** Lời nói, hành vi và workaround của user phải được tách khỏi kết luận của nhóm.
5. **Không bảo vệ giả thuyết.** Evidence làm giả thuyết yếu đi cũng là evidence có giá trị.
6. **Không tuyên bố validated.** Chặng 3 là phần luyện kỹ năng, không phải một vòng field research chính thức.
