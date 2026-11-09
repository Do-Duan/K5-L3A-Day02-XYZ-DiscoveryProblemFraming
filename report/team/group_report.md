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
| 1 | Huy | Khi tiếp nhận phản hồi từ khách hàng qua form khảo sát hoặc ticket khiếu nại, tôi muốn phân loại các nhóm lỗi phổ biến nhất trong tuần, để chuyển đúng cho đội kỹ thuật xử lý kịp thời. | Nhân viên Customer Support (CS) / Product Team. | tốn khoảng 40 phút/ngày, lặp đi lặp lại, dễ bị thiên kiến hoặc sai sót. | Ticket nhận về expect có bao nhiêu nhãn -> đơn vị xử lý các ticket đó là ai -> mỗi bước tốn khoảng bao nhiêu thời gian |
| 2 | Huy | Khi kết thúc các buổi họp giao ban hàng tuần, tôi muốn ghi nhận nhanh các quyết định và action items, để phân công công việc kịp thời mà không bị sót ý hay hiểu lầm. | Người ghi chép (PM / thư ký / lead) | Bước 1 (vừa họp vừa ghi dễ sót ý, mất tập trung) và Bước 3, 4 (sắp xếp và gõ lại mất 30-45 phút). | Hướng giải quyết sử dụng AI sẽ giải quyết như thế nào |
| 3 | Huy | Khi mở ứng dụng chat công việc sau 1 ngày nghỉ phép, tôi muốn nắm bắt ngay các quyết định hoặc sự cố đã giải quyết, để bắt nhịp lại luồng công việc mà không cần cuộn đọc từng tin một. | Nhân viên nghỉ phép quay lại làm (hoặc đồng nghiệp cùng ca). | (Đọc lướt và lọc thông tin): tốn 15-20 phút, nhiễu loạn thông tin. | Thời gian nghỉ phép không nhiều, không có quá nhiều giá trị |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | Duẩn|Khi kế toán trưởng cần kiểm tra, đối soát toàn bộ thu chi của 1 tháng, muốn truy xuất nhanh chóng các dữ liệu giao dịch đã ghi nhận, để không phải dò dẫm thủ công qua hơn 100 trang sổ viết tay |Kế toán trưởng / Quản lý tài chính | Mỗi lần phải kiểm tra hơn 100 trang sổ sách,mất thời gian và dễ sai sót |Tại sao tổ chức vẫn duy trì việc ghi chép sổ sách thủ công bằng tay với quy mô 100+ trang/tháng thay vì bắt buộc sử dụng phần mềm kế toán từ trước? |
| 8 | Duẩn| Khi đến cuối tuần, kế toán viên cần tổng hợp gần 50 hóa đơn giao dịch phát sinh trong tuần qua để ghi nhận vào sổ sách chung |Kế toán viên / Nhân viên tài chính nội bộ |Mỗi lần ghi chép tốn gần 2 tiếng |Liệu thời gian tốn 2 tiếng mỗi tuần có phải là một 'nỗi đau' thực sự cần can thiệp công nghệ cao (như AI/Workflow phức tạp), hay chỉ cần chuẩn hóa lại biểu mẫu nhập liệu Excel và quy định các phòng ban nộp hóa đơn đúng chuẩn định dạng (Rule đơn giản) là đã giải quyết triệt để? |
| 9 | Duẩn|Khi tham gia các cuộc họp kéo dài với nhiều nội dung thảo luận và phân công công việc khác nhau, tôi muốn tự động ghi nhận, bóc tách và tóm tắt thành các ý chính kèm theo danh sách việc cần làm (action items), để không bị quên mất hoặc nhầm lẫn nhiệm vụ được giao sau cuộc họp | Nhân viên văn phòng / Trưởng nhóm dự án / Thành viên tham gia họp|Quên mất hoặc nhầm lẫn một số nội dung của cuộc họp |Nếu dùng AI để tự động sinh biên bản họp hoàn hảo mà các thành viên vẫn không thèm đọc hoặc không cập nhật trạng thái thực thi thì bài toán cốt lõi có được giải quyết không? |
| 10 | Dũng | Khi giáo viên gửi danh sách học viên mới đầu tuần tập huấn, tôi muốn đưa thông tin vào hệ thống nhanh, để học viên kịp lịch tập huấn | Nhân viên(tôi), giáo viên dạy lái, học viên | Bước 4 gõ vào hệ thống khoảng 3 phút/hồ sơ. | nhập khoảng 150 hồ sơ/tuần, mỗi hồ sơ gõ khoảng 3 phút, và có hôm phải chờ giáo viên nộp hồ sơ cứng cả ngày. Nếu thời gian chờ còn dài hơn thời gian gõ thì AI giải quyết được phần nào? Nếu giáo viên nộp theo form chuẩn thì bước gõ có giảm không? |
| 11 | Dũng | Khi nhiều giáo viên gửi hồ sơ cùng lúc qua nhiều kênh, tôi muốn biết cái nào thiếu và cái nào đã đủ, để xử lý theo thứ tự hợp lý | Nhân viên nhập hồ sơ (tôi), 5 giáo viên dạy lái | Bước 2, mở từng hồ sơ đối chiếu thủ công mất khoảng 2 phút/hồ sơ. Chỗ thiếu thường lộ ra muộn, khi đã nhập dở | khoảng 3 lần bỏ sót mỗi tuần vì hồ sơ thiếu thông tin và bị than khoảng 4 lần mỗi tuần. Trung tâm đã từng có danh sách giấy tờ bắt buộc cho giáo viên chưa? Nếu có mà vẫn thiếu thì danh sách đó sai ở chỗ nào, nếu chưa có thì tại sao chưa thử làm trước khi dùng AI? |
| 12 | Dũng | Khi giáo viên hỏi vì sao hồ sơ của họ chưa nhập, tôi muốn biết ngay hồ sơ đang ở bước nào, để trả lời được ngay | Nhân viên(tôi), giáo viên dạy lái, học viên | Bước 2, tìm hồ sơ ở nhiều chỗ, chiếm phần lớn trong 2-3 phút mỗi lần hỏi. Hồ sơ không có một nơi ghi trạng thái chung nên phải tìm lại mỗi lần | hồ sơ đang ở đâu mỗi ngày, mỗi lần 2-3 phút, và thất lạc 2-3 lần mỗi tháng. Trong hệ thống bạn nhập hiện có biết được học viên nào đã nhập chưa không? Nếu có thì vì sao vẫn phải đi tìm hồ sơ, và việc tìm là tìm hồ sơ cứng hay tìm trong tin nhắn? |

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A | | |
| B | | |
| C | | |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: 
├── Opportunity A: 
├── Opportunity B: 
└── Opportunity C: 
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

-

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| | | | | | | | | |
| | | | | | | | | |
| | | | | | | | | |

**Candidate được chọn:**

**Vì sao chọn:**

**Vì sao loại các candidate còn lại:**

**Xử lý bất đồng (nếu có):**

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm kiểm chứng trong buổi này:

### 3.2. Kiểm chứng

Cách đã dùng: Phỏng vấn / Survey / Log, ticket, review

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | |
| Câu nói đáng nhớ nhất (nguyên văn) | |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | |
| Hiện đang xử lý bằng cách nào (workaround)? | |
| Mất bao lâu, bao lần? | |
| Insight / opportunity rút ra | |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| | | | |

**Nhóm đã sửa problem thế nào sau kiểm chứng:**

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| | | | | | |
| | | | | | |
| | | | | | |

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text

```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |

**Bottleneck chính:**

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text

```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | | | |
| Tổng thời gian | | | |
| Số bước thủ công | | | |
| Bottleneck chính | | | |
| Rủi ro mới phát sinh | | | |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

-

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô:

Vì sao:

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | | | | |
| **Rule** | | | | |
| **Workflow** | | | | |
| **Agent** | | | | |

**Mức chọn:**

**Vì sao không chọn mức đơn giản hơn:**

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | |
| **Judgment** — con người cân nhắc, quyết định gì? | |
| **Action** — hành động cuối cùng là gì, ai làm? | |
| **Outcome** — đo kết quả bằng gì? | |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? Bằng chứng:
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? Vì sao, và thiết kế đã xử lý thế nào:

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | |
| **Quy trình** | |
| **Bottleneck** | |
| **Impact** | |
| **Success Metric** (baseline → target, cách đo) | |
| **Boundary** | |
| **AI intervention point** | |
| **Mức chọn** | No AI / Rule / Workflow / Agent |
| **Rủi ro & người kiểm tra** | |

**Thay đổi so với v0 và lý do:**

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| | | | |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

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
