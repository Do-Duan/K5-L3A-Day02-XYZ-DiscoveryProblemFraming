# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: XYZ
- Thành viên: xem `TEAM.md`
- Candidate problem được chọn (1 câu):
- Quyết định cuối: Go / Not Yet / No-Go

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Huy | Khi tiếp nhận phản hồi từ khách hàng qua form khảo sát hoặc ticket khiếu nại, tôi muốn phân loại các nhóm lỗi phổ biến nhất trong tuần, để chuyển đúng cho đội kỹ thuật xử lý kịp thời. | Nhân viên Customer Support (CS) / Product Team. | tốn khoảng 40 phút/ngày, lặp đi lặp lại, dễ bị thiên kiến hoặc sai sót. | Ticket nhận về expect có bao nhiêu nhãn -> đơn vị xử lý các ticket đó là ai -> mỗi bước tốn khoảng bao nhiêu thời gian (Đức) |
| 2 | Huy | Khi kết thúc các buổi họp giao ban hàng tuần, tôi muốn ghi nhận nhanh các quyết định và action items, để phân công công việc kịp thời mà không bị sót ý hay hiểu lầm. | Người ghi chép (PM / thư ký / lead) | Bước 1 (vừa họp vừa ghi dễ sót ý, mất tập trung) và Bước 3, 4 (sắp xếp và gõ lại mất 30-45 phút). | Hướng giải quyết sử dụng AI sẽ giải quyết như thế nào (Đức) |
| 3 | Huy | Khi mở ứng dụng chat công việc sau 1 ngày nghỉ phép, tôi muốn nắm bắt ngay các quyết định hoặc sự cố đã giải quyết, để bắt nhịp lại luồng công việc mà không cần cuộn đọc từng tin một. | Nhân viên nghỉ phép quay lại làm (hoặc đồng nghiệp cùng ca). | (Đọc lướt và lọc thông tin): tốn 15-20 phút, nhiễu loạn thông tin. | Thời gian nghỉ phép không nhiều, không có quá nhiều giá trị (Đức và Dũng) |
| 4 | Đức | Khi nhận file settlement buổi sáng từ các cổng thanh toán, Mai muốn biết giao dịch nào chưa khớp với đơn trên hệ thống bán hàng, để xử lý lệch trước khi ghi sổ doanh thu trong ngày | Kế toán | rà dòng lệch: khoảng 25 phút. Mỗi dòng phải mở 2 hệ thống, dù nguyên nhân thường lặp lại (hoàn một phần, đơn tách, lệch ngày) | Các công cụ quản lý doanh nghiệp hiện tại đã làm tốt công việc này chưa? tự động hóa chưa? chi phí thế nào? |
| 5 | Đức | Khi sao kê có khoản tiền vào với nội dung chuyển khoản không chuẩn, tôi muốn xác định khoản đó thuộc đơn hoặc khách nào, để gạch công nợ và xác nhận đơn đúng | Kế toán, CSKH | đoán và hỏi: khoảng 30 phút. Kết quả phụ thuộc trí nhớ và việc người khác có trả lời kịp không | Việc này có thường xuyên xảy ra không? có value thực sự? |
| 6 | Đức | Khi sếp hỏi “hôm nay tiền về bao nhiêu, còn bao nhiêu”, Mai muốn trả lời bằng số đã đối soát trong vài phút, để sếp quyết định duyệt chi ngay | CEO, Kế toán | Số liệu nằm rải rác ở nhiều portal | task bất chợt nên khó đo lường baseline |
| 7 | Duẩn|Khi kế toán trưởng cần kiểm tra, đối soát toàn bộ thu chi của 1 tháng, muốn truy xuất nhanh chóng các dữ liệu giao dịch đã ghi nhận, để không phải dò dẫm thủ công qua hơn 100 trang sổ viết tay |Kế toán trưởng / Quản lý tài chính | Mỗi lần phải kiểm tra hơn 100 trang sổ sách,mất thời gian và dễ sai sót |Tại sao tổ chức vẫn duy trì việc ghi chép sổ sách thủ công bằng tay với quy mô 100+ trang/tháng thay vì bắt buộc sử dụng phần mềm kế toán từ trước? |
| 8 | Duẩn| Khi đến cuối tuần, kế toán viên cần tổng hợp gần 50 hóa đơn giao dịch phát sinh trong tuần qua để ghi nhận vào sổ sách chung |Kế toán viên / Nhân viên tài chính nội bộ |Mỗi lần ghi chép tốn gần 2 tiếng |Liệu thời gian tốn 2 tiếng mỗi tuần có phải là một 'nỗi đau' thực sự cần can thiệp công nghệ cao (như AI/Workflow phức tạp), hay chỉ cần chuẩn hóa lại biểu mẫu nhập liệu Excel và quy định các phòng ban nộp hóa đơn đúng chuẩn định dạng (Rule đơn giản) là đã giải quyết triệt để? |
| 9 | Duẩn|Khi tham gia các cuộc họp kéo dài với nhiều nội dung thảo luận và phân công công việc khác nhau, tôi muốn tự động ghi nhận, bóc tách và tóm tắt thành các ý chính kèm theo danh sách việc cần làm (action items), để không bị quên mất hoặc nhầm lẫn nhiệm vụ được giao sau cuộc họp | Nhân viên văn phòng / Trưởng nhóm dự án / Thành viên tham gia họp|Quên mất hoặc nhầm lẫn một số nội dung của cuộc họp |Nếu dùng AI để tự động sinh biên bản họp hoàn hảo mà các thành viên vẫn không thèm đọc hoặc không cập nhật trạng thái thực thi thì bài toán cốt lõi có được giải quyết không? |
| 10 | Dũng | Khi giáo viên gửi danh sách học viên mới đầu tuần tập huấn, tôi muốn đưa thông tin vào hệ thống nhanh, để học viên kịp lịch tập huấn | Nhân viên(tôi), giáo viên dạy lái, học viên | Bước 4 gõ vào hệ thống khoảng 3 phút/hồ sơ. | nhập khoảng 150 hồ sơ/tuần, mỗi hồ sơ gõ khoảng 3 phút, và có hôm phải chờ giáo viên nộp hồ sơ cứng cả ngày. Nếu thời gian chờ còn dài hơn thời gian gõ thì AI giải quyết được phần nào? Nếu giáo viên nộp theo form chuẩn thì bước gõ có giảm không? |
| 11 | Dũng | Khi nhiều giáo viên gửi hồ sơ cùng lúc qua nhiều kênh, tôi muốn biết cái nào thiếu và cái nào đã đủ, để xử lý theo thứ tự hợp lý | Nhân viên nhập hồ sơ (tôi), 5 giáo viên dạy lái | Bước 2, mở từng hồ sơ đối chiếu thủ công mất khoảng 2 phút/hồ sơ. Chỗ thiếu thường lộ ra muộn, khi đã nhập dở | khoảng 3 lần bỏ sót mỗi tuần vì hồ sơ thiếu thông tin và bị than khoảng 4 lần mỗi tuần. Trung tâm đã từng có danh sách giấy tờ bắt buộc cho giáo viên chưa? Nếu có mà vẫn thiếu thì danh sách đó sai ở chỗ nào, nếu chưa có thì tại sao chưa thử làm trước khi dùng AI? |
| 12 | Dũng | Khi giáo viên hỏi vì sao hồ sơ của họ chưa nhập, tôi muốn biết ngay hồ sơ đang ở bước nào, để trả lời được ngay | Nhân viên(tôi), giáo viên dạy lái, học viên | Bước 2, tìm hồ sơ ở nhiều chỗ, chiếm phần lớn trong 2-3 phút mỗi lần hỏi. Hồ sơ không có một nơi ghi trạng thái chung nên phải tìm lại mỗi lần | hồ sơ đang ở đâu mỗi ngày, mỗi lần 2-3 phút, và thất lạc 2-3 lần mỗi tháng. Trong hệ thống bạn nhập hiện có biết được học viên nào đã nhập chưa không? Nếu có thì vì sao vẫn phải đi tìm hồ sơ, và việc tìm là tìm hồ sơ cứng hay tìm trong tin nhắn? |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Nhập / phân loại dữ liệu thô |Nhập 150 hồ sơ/tuần, nhập hóa đơn hằng tuần vào sổ, phân loại lỗi từ phản hồi khách hàng  |Đọc từng bản ghi thô (giấy, ảnh, văn bản) rồi gõ hoặc gắn nhãn lặp đi lặp lại |
| B — Đối soát / kiểm tra khớp |Đối soát tiền cổng thanh toán, xử lý tiền chuyển khoản treo, hồ sơ thiếu thông tin bị bỏ sót, kiểm xuất 1 tháng giao dịch từ sổ viết tay |So hai nguồn (hoặc so với danh sách chuẩn) để tìm chỗ lệch, chỗ thiếu rồi dò nguyên nhân |
| C — Tổng hợp nội dung họp / chat |Ghi chép biên bản họp, tổng hợp nội dung sau cuộc họp, theo kịp group chat sau thời gian nghỉ |Gom nội dung dài, rời rạc rồi rút ra quyết định và việc cần làm cho người khác đọc |
| D — Tra cứu trạng thái |Bị hỏi trạng thái và nghi thất lạc hồ sơ, trả lời sếp về tình hình tiền |Bị hỏi bất chợt, phải đi tìm ở nhiều chỗ mới trả lời được vì không có một nơi ghi trạng thái chung|

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian nhân viên văn phòng mất cho việc xử lý thủ công dữ liệu thô (hiện khoảng 25–120 phút mỗi lần/đợt) mà không tăng sai sót
├── Opportunity A: Phải đọc rồi gõ hoặc gắn nhãn lại từng bản ghi thô (hồ sơ, hóa đơn, phản hồi) nên tốn thời gian và dễ nhập sai
├── Opportunity B:Khó phát hiện sớm chỗ lệch hoặc thiếu giữa các nguồn (giao dịch, hồ sơ, sổ sách) nên mất nhiều công dò nguyên nhân
├── Opportunity C: Khó rút ra quyết định và việc cần làm từ nội dung dài, rời rạc (họp, chat) nên dễ sót việc, dễ hiểu nhầm
└── Opportunity D: Phải đi tìm ở nhiều nơi mới trả lời được câu hỏi về trạng thái hoặc số hiện tại nên trả lời chậm, việc đang làm bị ngắt quãng
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- “Cần hệ thống tự động phân loại và trích xuất dữ liệu từ hóa đơn”. Đây là cách giải. Nhu cầu thật nằm ở Opportunity A: phải gõ lại từng hóa đơn.
- “Cần AI Speech-to-Text ghi âm và tóm tắt cuộc họp” . Nhu cầu thật là Opportunity C: dễ sót action item sau họp.
- “Cần chatbot hoặc hỏi bằng câu tự nhiên để biết hồ sơ/tiền đang ở đâu” . Nhu cầu thật là Opportunity D: không có một nơi ghi trạng thái chung.
- “Cần dashboard dòng tiền hoặc bảng theo dõi trạng thái” . Đây cũng là một cách giải, còn nhu cầu thật vẫn là Opportunity D.
- “Số hóa sổ viết tay sang Excel hoặc phần mềm kế toán” . Nhu cầu thật là Opportunity B: dò số liệu thủ công qua hơn 100 trang.
- “Tự động tạo ticket Jira và assign cho Dev”. Đây là cách xử lý, không phải nhu cầu của người dùng.


### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **#1. Phân loại phản hồi / ticket khiếu nại (Huy)** | 5 | 4 | 5 | 5 | 5 | 5 | 4 | **33** |
| **#4. Đối soát settlement cổng thanh toán (Đức)** | 4 | 5 | 4 | 4 | 3 | 4 | 4 | **28** |
| **#10. Nhập hồ sơ học viên lái xe (Dũng)** | 4 | 3 | 4 | 4 | 3 | 3 | 5 | **26** |
| **#2 & #9. Tóm tắt biên bản họp & action items (Huy & Duẩn)** | 4 | 3 | 3 | 3 | 4 | 3 | 4 | **24** |
| **#7. Truy xuất & đối soát sổ tay 100+ trang (Duẩn)** | 3 | 2 | 4 | 3 | 2 | 2 | 3 | **19** |

**Candidate được chọn:**
Candidate #1: Phân loại phản hồi từ khách hàng / người dùng để điều phối xử lý kịp thời (áp dụng cho trực page bán hàng part-time hoặc xử lý form feedback sự kiện CLB).

**Vì sao chọn:**
1. **Vừa sức lab nhất (Feasibility cao):** Dễ dàng tìm được dataset mẫu (Kaggle/HuggingFace) hoặc tự tạo 30-50 dòng mock data từ Google Form. Xử lý text phi cấu trúc là thế mạnh rõ ràng nhất của LLM để demo trong môn học.
2. **So sánh rõ rệt các mức độ can thiệp:** Cho phép nhóm dễ dàng thiết kế lab để so sánh sự khác biệt giữa Rule (if/else từ khóa) vs. Workflow (prompt chain phân loại) vs. Agent (tự động phân luồng).
3. **Đo lường được ngay (Impact):** Có thể đo thời gian một bạn đọc và phân loại bằng tay 50 dòng feedback trên Google Sheets so với dùng script API.

**Vì sao loại các candidate còn lại:**
- **#4 (Đối soát cổng thanh toán) & #7 (Sổ kế toán):** Bài toán kế toán cần sự chính xác 100%. Cách giải quyết đúng đắn nhất là chuẩn hóa phần mềm (No AI) hoặc viết script Excel/Python (Rule). Dùng AI tạo sinh (LLM) để cộng trừ đối soát tài chính trong lab là sai mục đích sử dụng và dễ bị hallucination sai số.
- **#10 (Nhập hồ sơ học viên):** Vướng rào cản thao tác vật lý (nhận giấy tờ). Cách giải No AI (bắt buộc dùng Google Form chuẩn ngay từ đầu) giải quyết triệt để hơn là cố nhét AI vào việc nhập liệu lại.
- **#2 & #9 (Tóm tắt họp):** Khó lấy được data thật (recording họp nội bộ thường bảo mật), và thị trường đã có sẵn các tool như Otter.ai hay Zoom Companion làm quá tốt, nhóm khó tạo ra giá trị mới mẻ trong bài lab.

**Xử lý bất đồng (nếu có):**
Nhóm từng phân vân candidate #4 (kế toán) do Đức hiểu rất rõ quy trình. Tuy nhiên, khi đánh giá tiêu chí "So sánh được No AI / Rule / AI", nhóm nhận ra bài toán số liệu tài chính giải bằng No AI (chuẩn hóa luồng) hoặc Rule (code logic khớp mã) là tối ưu nhất. Vì vậy, nhóm chốt chọn #1 để tận dụng đúng không gian NLP/Text classification của môn học AI.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Người dùng (trực page/ban sự kiện) sẵn sàng tin nhãn do AI gán thay vì tự đọc từng dòng | Usability | 5 | 2 | Có |
| 2 | Prompt có thể phân loại đúng >80% các phản hồi có ngôn ngữ lóng, sai chính tả của sinh viên/khách hàng | Feasibility | 5 | 3 | Có |
| 3 | AI giúp giảm thời gian phân loại xuống tính bằng giây, thay vì 30-40 phút lướt Google Sheets | Value | 4 | 3 | Không |
| 4 | Có đủ dữ liệu mẫu (mock data hoặc open dataset) sát thực tế để làm bài lab | Feasibility | 4 | 4 | Không |

Giả định nhóm kiểm chứng trong buổi này:
**Giả định #1 và #2:** Liệu đọc lướt nhãn AI gán có nhanh hơn thật không, hay người dùng vẫn không tin và phải đọc lại toàn bộ text gốc; và text thực tế viết tắt, lủng củng thì AI có bắt được ý không.

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn chéo bạn học trong lớp (từng làm part-time trực page/CSKH hoặc Ban Sự kiện CLB) + Review nhanh 20 dòng sample text giả lập.

Interview snapshot:

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | Một bạn sinh viên lớp kế bên, từng trực page bán áo thun part-time và quản lý form feedback sự kiện CLB. |
| Câu nói đáng nhớ nhất (nguyên văn) | *"Đọc form feedback sự kiện mờ cả mắt. Nhiều lúc form có 100 responses, đọc đến dòng 30 là lú luôn, toàn phải tự add thêm một cột trên Excel rồi gõ tay tag 'chê đồ ăn', 'lỗi link', 'khen' để cuối ngày báo cáo."* |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Đợt CLB tổ chức sự kiện tuần trước, có trục trặc link đăng ký. Sinh viên nhắn tin vào page và điền form dồn dập, mất gần 45 phút copy/paste và gom nhóm lỗi để báo ban Kỹ thuật sửa link. |
| Hiện đang xử lý bằng cách nào (workaround)? | Export Google Sheets, dùng filter (bộ lọc) Ctrl+F từ khóa "lỗi", "không được", rồi gắn nhãn thủ công từng dòng. |
| Mất bao lâu, bao lần? | Tốn 30-45 phút mỗi đợt chốt form/ca trực. |
| Insight / opportunity rút ra | Bạn này không cần AI tự động reply khách. Bạn ấy chỉ cần AI đọc cái sheet đó, gán sẵn tag (VD: Lỗi kỹ thuật, Hỏi thông tin, Phàn nàn) vào cột bên cạnh để bạn ấy chỉ việc lướt mắt kiểm tra rồi đem báo cáo. |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Phỏng vấn chéo sinh viên | 2 người | Rất mất thời gian khi phải gom nhóm ý kiến lộn xộn. Sẵn sàng dùng tool nếu nó tích hợp thẳng vào file Excel/Sheets. | Nếu AI gán nhãn sai 1-2 lần đầu, họ sẽ mất lòng tin và thà tự đọc tay từ đầu cho chắc ăn. Cần có cơ chế giải thích lý do ngắn gọn. |
| Review sample text (20 dòng) | 20 mẫu câu | Nhiều câu không có từ khóa rõ ràng ("app dỏm thế", "ấn mãi chả hiện gì"), dùng Rule if/else tìm từ khóa "lỗi" sẽ bị trượt. | Vẫn có những câu chung chung ("không thích lắm") khó để AI xếp vào một nhóm kỹ thuật cụ thể. |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**
Nhóm nhận ra rào cản Usability (mất niềm tin nếu AI sai). Vì vậy, rút gọn scope: AI không tự động gửi ticket đi, mà chỉ làm nhiệm vụ "Drafting/Tagging" trên bảng tính. Output của AI phải bao gồm 2 cột: `Nhãn (Label)` và `Lý do trích xuất (Trích 3-4 chữ từ câu gốc)`. Việc có cột "Lý do" giúp người dùng lướt kiểm tra (Human-in-the-Loop) cực nhanh mà không cần đọc hết câu dài.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **Google Sheets - Bộ lọc / IF(SEARCH())** | Tính năng sẵn có | Dùng hàm dò từ khóa (Rule) để phân loại | Miễn phí, sẵn có, chạy ngay trên file làm việc | Chỉ bắt được từ khóa tĩnh, sai chính tả là trượt, không hiểu ngữ cảnh câu dài | Sẽ dùng cách này làm Baseline (No AI/Rule) để so sánh hiệu năng trong Lab. |
| **Tiện ích GPT for Sheets** | workspace.google.com/marketplace | Gọi hàm `=GPT_CLASSIFY()` trực tiếp trong ô Sheets | Nhanh, đáp ứng đúng nhu cầu xử lý hàng loạt trên bảng tính | Trả phí token, prompt mặc định đôi khi trả về format lung tung không đúng bộ nhãn | Cần thiết kế Workflow/Prompt kỹ lưỡng (Few-shot, ép output JSON/chuẩn nhãn) thay vì dùng prompt zero-shot trần. |
| **Zendesk / Freshdesk** | zendesk.com | Phân luồng ticket tự động toàn hệ thống | Chuyên nghiệp, độ chính xác cao cho doanh nghiệp | Quá cồng kềnh, đắt tiền, không phù hợp cho các quy mô nhỏ (CLB, part-time) hoặc để làm mini-lab | Giải pháp lab của nhóm (gọi API phân loại nhẹ) sẽ là phiên bản "micro" thay thế giá rẻ, tập trung xử lý khâu bottleneck nhất. |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
HIỆN TẠI — 5 bước, 45 phút sau mỗi buổi họp (ước lượng), 5/5 bước thủ công

[1 Họp + ghi chú nhanh: trong buổi họp]
→ [2 Đọc lại ghi chú, chắp vá chỗ thiếu: 15'] ← BOTTLENECK
→ [3 Soạn biên bản (Word): 20'] ← BOTTLENECK
→ [4 Lọc action items, phân công: 7']
→ [5 Gửi email / chat nhóm: 3']
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 |Người ghi chép (PM / thư ký / lead) |Nội dung buổi họp | Ghi chú thô (tay hoặc laptop)|Trong buổi họp; 1–2 buổi/tuần | Vừa họp vừa ghi nên dễ sót ý|
| 2 |Người ghi chép |Ghi chú thô |Ghi chú đã bổ sung chỗ thiếu |15' |Ghi chú lộn xộn, phải chắp vá |
| 3 | Người ghi chép|Ghi chú đã bổ sung | Biên bản họp (Word)|20' | Gõ lại toàn bộ|
| 4 | Người ghi chép|Biên bản |Danh sách việc: người phụ trách, hạn |7' (ước lượng) |Dễ sót action item (~20%) |
| 5 |Người ghi chép → thành viên họp | Biên bản và danh sách việc|Thông báo đến cả nhóm| 3'|Thành viên hay nhắn hỏi lại “việc này deadline bao giờ” |

**Bottleneck chính:**: Bước 2 và 3 (đọc lại ghi chú và soạn biên bản): khoảng 35 phút mỗi buổi, 1–2 buổi mỗi tuần.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
TƯƠNG LAI — 4 bước, khoảng 10 phút, 2/4 bước thủ công

[1 Lấy bản ghi âm / transcript buổi họp: ~1']          ← CÔNG CỤ (tự động)
→ [2 Tóm tắt: quyết định + action items (người, hạn)
     vào template biên bản chuẩn: ~2']                  ← AI (chỉ tạo bản nháp)
→ [3 Người ghi chép đối chiếu với ghi chú, sửa: ~5']    ← CON NGƯỜI
→ [4 Gửi biên bản: ~1']                                  ← CON NGƯỜI

RULE: template biên bản cố định (mục quyết định, mục action item gồm người và hạn).
BOUNDARY: AI không tự gửi biên bản, không tự giao việc hay đặt deadline,
          không thêm quyết định không có trong buổi họp; chỉ dùng nội dung buổi họp đó.
          Người luôn kiểm tra tên người phụ trách và deadline trước khi gửi.
PHƯƠNG ÁN QUAY VỀ: bản nháp thiếu hoặc sai nhiều (transcript lỗi, thuật ngữ nội bộ)
          → bỏ bản nháp, soạn theo template cũ từ ghi chú tay.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 5| 4| |
| Tổng thời gian | 45 phút| dưới 10' |Target chính dưới 10' (Huy); Duẩn đặt dưới 5' |
| Số bước thủ công |5/5 |2/4 | Người vẫn kiểm tra và gửi|
| Bottleneck chính |Đọc lại ghi chú + soạn biên bản |Người kiểm tra + sửa bản nháp | Chấp nhận được vì là điểm kiểm soát chất lượng|
| Rủi ro mới phát sinh |Không | AI gán sai người phụ trách hoặc deadline, bịa quyết định, nhầm thuật ngữ nội bộ, lộ nội dung họp| Xử lý bằng boundary, người duyệt và phương án quay về|

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** |Người ghi chép biên bản (PM / thư ký / lead) cho các thành viên tham gia họp |
| **Quy trình** |Sau mỗi buổi họp: đọc lại ghi chú, soạn biên bản, lọc action items, gửi nhóm|
| **Bottleneck** |Đọc lại ghi chú và soạn biên bản mất khoảng 35 phút, vì vừa họp vừa ghi nên dễ sót ý |
| **Impact** |45 phút/buổi, 1–2 buổi/tuần; thành viên nhắn hỏi lại deadline, dễ quên việc được giao |
| **Success Metric** (baseline → target, cách đo) |Thời gian 45' → dưới 10'/buổi; sót action item 20% → dưới 2%. Đo bằng cách bấm giờ 5 buổi gần nhất, rồi 4 tuần pilot, đối chiếu với danh sách chốt cuối |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | AI chỉ tạo bản nháp, không tự gửi, không tự giao việc, không bịa quyết định. Người luôn kiểm tra người phụ trách và deadline trước khi gửi|

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- AI chỉ ra metric chỉ đo tốc độ và tỉ lệ sót việc, chưa đo độ đúng của nội dung (gán sai người phụ trách hoặc deadline), và baseline 45' / 20% mới là ước lượng. Nhóm đồng ý, thêm metric chất lượng ở v1 và ghi rõ baseline là ước lượng sẽ đo lại. Boundary được bổ sung điều kiện xin phép khi ghi âm.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở mức **độ mơ hồ trung bình, độ phức tạp thấp–trung bình**: lời nói trong họp có thể thiếu rõ ràng, nhưng đầu ra cần tạo khá cố định (quyết định và action items theo mẫu).

Vì sao: AI cần hiểu transcript để tóm tắt và trích người phụ trách, deadline; còn template, bước kiểm tra và gửi đã có quy trình rõ.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Dùng template và checklist; người vẫn đọc lại, gõ biên bản và tổng hợp việc. | Khi số buổi họp ít hoặc thời gian hiện tại chấp nhận được. | Vẫn mất khoảng 35 phút đọc lại và soạn; dễ sót việc. | Chưa chọn |
| **Rule** | Template cố định, quy tắc kiểm tra mục quyết định, người phụ trách và deadline. | Đủ để chuẩn hóa định dạng và báo trường còn thiếu. | Không tự hiểu được ghi chú/transcript tự nhiên, lộn xộn. | Dùng hỗ trợ |
| **Workflow** | Công cụ lấy transcript → AI tạo nháp theo template → người ghi chép kiểm tra, sửa và gửi. | Khi AI giúp rút thời gian soạn, còn người kiểm tra trước khi gửi. | AI có thể tóm tắt sai hoặc gán nhầm người/hạn; cần kiểm tra và phương án quay về. | **Chọn** |
| **Agent** | AI tự quyết định nội dung, giao việc hoặc gửi biên bản. | Chỉ cân nhắc nếu cần tự chủ và độ tin cậy đã được chứng minh. | Có thể bịa quyết định, giao sai việc hoặc gửi nội dung chưa duyệt. | Không chọn |

**Mức chọn:** Workflow, AI chỉ tạo bản nháp; con người kiểm tra và quyết định gửi.

**Vì sao không chọn mức đơn giản hơn:** Template/Rule chỉ chuẩn hóa biểu mẫu, không chắt lọc được quyết định và action items từ lời nói tự nhiên. AI hỗ trợ đúng bước tốn thời gian; người vẫn duyệt để giảm rủi ro.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Bản nháp tóm tắt quyết định và action items, gồm người phụ trách, deadline, theo template. |
| **Judgment** — con người cân nhắc, quyết định gì? | Người ghi chép đối chiếu với transcript/ghi chú, sửa nội dung, người và hạn; quyết định có thể gửi chưa. |
| **Action** — hành động cuối cùng là gì, ai làm? | Người ghi chép gửi biên bản đã duyệt; AI không tự gửi hoặc giao việc. |
| **Outcome** — đo kết quả bằng gì? | Thời gian 45 phút xuống dưới 10 phút/buổi; tỷ lệ sót việc ước lượng 20% xuống dưới 2%; đo lại trong pilot. |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Transcript hoặc bản ghi âm được phép dùng, cùng template; ghi chú hiện có, transcript cần được tạo. |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Ghi lại các lỗi/sửa của người duyệt như sót việc, sai người/hạn; dùng để chỉnh prompt và checklist. |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng: **Được hỗ trợ**. Người ghi chép vẫn đối chiếu và duyệt biên bản; AI không tự gửi hay phân công.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào: **Bỏ sót action item** có thể khiến việc không được làm; báo nhầm người hoặc deadline cũng gây rối. Người ghi chép kiểm tra bản nháp, nhất là quyết định, người phụ trách và hạn; nếu sai nhiều thì quay lại soạn từ ghi chú tay.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Người ghi chép biên bản (PM / thư ký / lead) và các thành viên dự họp. |
| **Quy trình** | Sau họp, lấy transcript được phép sử dụng, tạo bản nháp theo template, người ghi chép đối chiếu và sửa rồi gửi cho nhóm. |
| **Bottleneck** | Đọc lại ghi chú và soạn biên bản mất khoảng 35 phút/buổi; ghi chú nhanh dễ thiếu ý. |
| **Impact** | Tổng cộng khoảng 45 phút/buổi, 1–2 buổi/tuần; action item có thể bị sót, thành viên phải hỏi lại deadline. |
| **Success Metric** (baseline → target, cách đo) | Thời gian ước lượng 45' → dưới 10'/buổi; tỷ lệ sót action item ước lượng 20% → dưới 2%; độ chính xác người phụ trách/deadline ≥95%, không có quyết định bị AI tự thêm. Đo thời gian và đối chiếu bản nháp với biên bản đã duyệt trong 4 tuần pilot; đo lại baseline vì số hiện tại là ước lượng. |
| **Boundary** | Chỉ tạo bản nháp từ nội dung buổi họp; chỉ ghi âm khi người tham gia đồng ý. AI không tự gửi, giao việc, đặt deadline hay thêm quyết định. Người ghi chép phải kiểm tra nội dung, người phụ trách và hạn; sai nhiều thì quay về soạn theo template từ ghi chú tay. |
| **AI intervention point** | Sau khi có transcript: tóm tắt quyết định và đề xuất action items (nội dung, người phụ trách, deadline) vào template. |
| **Mức chọn** | **Workflow** — AI tạo nháp, người ghi chép duyệt và gửi. |
| **Rủi ro & người kiểm tra** | AI có thể sót việc, bịa quyết định hoặc gán sai người/hạn; người ghi chép kiểm tra với transcript/ghi chú trước khi gửi. |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Metric | Chỉ đo thời gian và tỷ lệ sót việc; baseline đang là ước lượng. | Thêm độ chính xác người phụ trách/deadline và yêu cầu không có quyết định tự thêm; đo lại baseline trong pilot. | Phản biện cho thấy cần đo chất lượng nội dung, không chỉ tốc độ. |
| Boundary | AI chỉ tạo nháp, không gửi/giao việc/bịa quyết định. | Bổ sung chỉ ghi âm khi có sự đồng ý; giữ người duyệt và phương án quay về. | Giảm rủi ro riêng tư và lỗi nội dung. |
| Mức can thiệp | Chưa chốt. | Workflow có người kiểm tra. | AI cần hiểu lời nói tự nhiên; Rule chỉ chuẩn hóa template, còn Agent có quyền quá rộng. |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Độ đầy đủ action items | Đối chiếu với transcript/ghi chú, không bỏ sót việc đã được giao. | Bỏ sót một việc đã được giao hoặc thêm việc không có trong buổi họp. |
| 2 | Đúng người phụ trách và deadline | Mọi người/hạn trong nháp khớp nội dung họp hoặc được đánh dấu chưa rõ để người ghi chép xác nhận. | Gán sai người/hạn hoặc tự đoán thông tin chưa được nêu. |
| 3 | Trung thực với nội dung họp | Tóm tắt đúng quyết định; không tự thêm quyết định, kết luận hay chi tiết. | Có nội dung không tìm thấy căn cứ trong transcript/ghi chú. |
| 4 | Đúng mẫu, dễ rà soát | Có đủ mục quyết định và action items theo template; câu chữ ngắn, rõ. | Thiếu mục, sai cấu trúc hoặc khó xác định việc cần làm. |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | | |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | | |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | | |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | | |

### 8.2. Kết luận

**Quyết định:** Go / Not Yet / No-Go

**Lý do:**

**Nếu Go — pilot nhỏ nhất:**

**Nếu Not Yet — cần kiểm chứng gì trước:**

**Nếu No-Go — nên làm gì thay AI:**

**Ngưỡng dừng** (nếu sau … mà … thì quay về …):

---

## 9. Hạn chế và hướng tiếp theo

-

## 10. Tài liệu tham khảo

-
