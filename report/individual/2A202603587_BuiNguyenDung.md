# Báo cáo cá nhân — MSSV_HoTen

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Bùi Nguyên Dũng
- MSSV: 2A202603587
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: XYZ
- Link repo nhóm: https://github.com/Do-Duan/K5-L3A-Day02-XYZ-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 |Lặp lại|Khi giáo viên gửi danh sách học viên mới, tôi muốn đưa thông tin vào hệ thống nhanh, để học viên kịp lịch tập huấn.  |Tôi, giáo viên dạy lái, học viên |Mỗi tuần nhập 150 bộ hồ sơ, có thể lâu hơn vì phải có hồ sơ cứng mới có thể nhập thông tin |
| 2 |Pain từ người khác |Khi giáo viên hỏi vì sao hồ sơ của họ chưa nhập, tôi muốn biết ngay hồ sơ đang ở bước nào, để trả lời được ngay.|Tôi, giáo viên dạy lái|Mỗi ngày đều có thể bị hỏi, ngay cả sau giờ làm, mỗi lần hỏi khoảng 2-3 phút |
| 3 |Pain từ người khác |Khi cần tìm hồ sơ một học viên, tôi muốn thấy nó ngay, để không bị coi là làm thất lạc. |Tôi, giáo viên dạy lái, học viên |Một tháng có thể bị thất lạc 2-3 lần, học viên có thể mất tiền đi photo công chứng lại|
| 4 |Tốn thời gian|Khi giáo viên gửi sửa thông tin học viên, tôi muốn cập nhật đúng người đúng trường, để không sai sót. |Tôi, giáo viên dạy lái|Trong tuần có 3 lần được yêu cầu phải sửa lại, trong đó có 1 lần sửa nhầm hoặc phải sửa lại cho đúng thông tin |
| 5 |Cần đọc, tổng hợp |Khi nhiều giáo viên gửi hồ sơ cùng lúc, tôi muốn biết cái nào thiếu và cái nào đã đủ, để xử lý theo thứ tự hợp lý. |Tôi, 5 giáo viên|Có khoảng 5 giáo viên gửi qua nhiều kênh nhắn tin, trong số đó có 3 lần bị bỏ sót vì thiếu thông tin |
| 6 |Pain từ người khác | Khi một số giáo viên thấy hồ sơ mình bị bỏ, tôi muốn có một căn cứ rõ ràng để giải thích, để không bị trách oan. |Tôi, giáo viên dạy lái |Trong tuần có khoảng 4 lần bị than chưa nhập người này vì thiếu thông tin cụ thể |


**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 |Nhập 150 hồ sơ/tuần chậm|Actor rõ, có quy trình, mất nhiều thời gian |Hồ sơ có đủ rõ để máy đọc không? Bottleneck là gõ tay hay chờ hồ sơ cứng? |
| 2 |Hồ sơ thiếu thông tin bị bỏ sót, nhiều kênh gửi |Có con số cụ thể. Bottleneck cụ thể: phát hiện thiếu quá muộn |Thiếu gì nhiều nhất? Có danh sách giấy tờ bắt buộc cố định không? |
| 3 |Bị hỏi trạng thái hồ sơ và nghi thất lạc |tần suất cao, đo được |Có dữ liệu để biết hồ sơ đang nằm ở đâu không? |

### Problem Card #1

| Trường | Nội dung |
|---|---|
| Job Story | Khi giáo viên gửi danh sách học viên mới đầu tuần tập huấn, tôi muốn đưa thông tin vào hệ thống nhanh, để học viên kịp lịch tập huấn|
| Actor |Nhân viên(tôi), giáo viên dạy lái, học viên |
| Thời điểm / bối cảnh |Đầu tuần, trước ngày tập huấn; nhập 150 bộ hồ sơ/tuần. Ngoài ra, đôi khi phải chờ giáo viên nộp hồ sơ cứng, có hôm mất cả ngày|
| Quy trình hiện tại (3–7 bước) |1. Nhận danh sách và hồ sơ · 2. Chờ đủ hồ sơ cứng · 3. Đối chiếu danh sách với hồ sơ · 4. Gõ từng học viên vào hệ thống · 5. Kiểm tra lại · 6. Báo giáo viên |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4 gõ vào hệ thống khoảng 3 phút/hồ sơ.|
| Impact (nếu không giải thì sao) |900 phút/tuần, trong đó riêng bước gõ 450 phút. Nếu không thì học viên trễ lịch, giáo viên tiếp tục hỏi|
| Success metric (baseline → target) |Tổng thời gian xử lý từ 6 phút xuống 3 phút/hồ sơ (với hồ sơ rõ nét); số lần sửa sai giữ ở mức hiện tại hoặc thấp hơn (hiện 1 lần/tuần). Kiểm chứng: bấm giờ 10 hồ sơ trước khi tin vào baseline |
| Phương án không dùng AI |Form chuẩn cho giáo viên, mẫu Excel có cột bắt buộc, giờ cắt nhận hồ sơ. Giảm thiếu sót nhưng chưa giảm thời gian gõ, vì hồ sơ giấy và ảnh chụp từ giáo viên vẫn phải gõ lại vào hệ thống |
| Giả thuyết về AI (nếu có) |AI đọc ảnh/scan hồ sơ rõ nét và điền sẵn các trường thành bản nháp; tôi kiểm tra và sửa trước khi lưu. Hồ sơ mờ hoặc viết tay vẫn nhập tay. Chỉ thử với dữ liệu đã che thông tin cá nhân (CCCD, địa chỉ) và khi trung tâm cho phép |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 6 phút/hồ sơ (chưa tính thời gian chờ)

[1 Nhận danh sách + hồ sơ: 1'] → [2 Chờ đủ hồ sơ cứng: chờ, có hôm cả ngày]
→ [3 Đối chiếu danh sách với hồ sơ: 1'] → [4 Gõ vào hệ thống: 3'] ← BOTTLENECK
→ [5 Kiểm tra lại: 1'] → [6 Báo giáo viên: theo lô]
```

### Problem Card #2

| Trường | Nội dung |
|---|---|
| Job Story |Khi nhiều giáo viên gửi hồ sơ cùng lúc qua nhiều kênh, tôi muốn biết cái nào thiếu và cái nào đã đủ, để xử lý theo thứ tự hợp lý |
| Actor |Nhân viên nhập hồ sơ (tôi), 5 giáo viên dạy lái |
| Thời điểm / bối cảnh |Suốt tuần, cao điểm đầu tuần; 5 giáo viên gửi qua nhiều kênh nhắn tin. Ngoài thời gian làm việc, sau khi hỏi giáo viên còn phải chờ bổ sung khoảng 60 phút mỗi lần|
| Quy trình hiện tại (3–7 bước) |1. Gom hồ sơ từ các kênh · 2. Mở từng hồ sơ, đối chiếu giấy tờ cần có · 3. Nhắn giáo viên hỏi phần thiếu · 4. Chờ bổ sung · 5. Nhập hồ sơ |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2, mở từng hồ sơ đối chiếu thủ công mất khoảng 2 phút/hồ sơ. Chỗ thiếu thường lộ ra muộn, khi đã nhập dở |
| Impact (nếu không giải thì sao) |120 phút/tuần cho việc kiểm tra và hỏi lại; bỏ sót 3 lần/tuần, bị kêu 4 lần/tuần. Nếu không giải: học viên có thể trễ lịch tập huấn, giáo viên mất niềm tin vào tiến độ |
| Success metric (baseline → target) |Kiểm tra và yêu cầu bổ sung từ 120 còn 40 phút/tuần; bỏ sót 3 còn 0 lần/tuần |
| Phương án không dùng AI |Danh sách giấy tờ bắt buộc dán sẵn, giáo viên tự tick trước khi gửi, chỉ nhận qua một kênh. Giảm hồ sơ thiếu nhưng tôi vẫn phải mở kiểm tra từng hồ sơ |
| Giả thuyết về AI (nếu có) |AI so từng hồ sơ với danh sách giấy tờ bắt buộc và liệt kê chỗ thiếu; tôi chỉ nhắn đúng phần thiếu |
| Cảm nhận nhanh | Rule hoặc Workflow|

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 120 phút/tuần cho kiểm tra và hỏi lại

[1 Gom hồ sơ từ các kênh] → [2 Mở từng hồ sơ, đối chiếu:] ← BOTTLENECK
→ [3 Nhắn giáo viên hỏi phần thiếu]
→ [4 Chờ bổ sung] → [5 Nhập hồ sơ]
```

### Problem Card #3

| Trường | Nội dung |
|---|---|
| Job Story | Khi giáo viên hỏi vì sao hồ sơ của họ chưa nhập, tôi muốn biết ngay hồ sơ đang ở bước nào, để trả lời được ngay |
| Actor |Nhân viên(tôi), giáo viên dạy lái, học viên |
| Thời điểm / bối cảnh |Hằng ngày đều bị hỏi, kể cả sau giờ làm; mỗi lần hỏi mất 2-3 phút |
| Quy trình hiện tại (3–7 bước) |1. Nhận câu hỏi · 2. Tìm hồ sơ ở các chỗ có thể (tin nhắn, giấy, file) · 3. Xác định đã nhập hay chưa · 4. Trả lời giáo viên |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 2, tìm hồ sơ ở nhiều chỗ, chiếm phần lớn trong 2-3 phút mỗi lần hỏi. Hồ sơ không có một nơi ghi trạng thái chung nên phải tìm lại mỗi lần |
| Impact (nếu không giải thì sao) |Thất lạc 2-3 lần/tháng, học viên mất tiền photo công chứng lại. Giáo viên mất niềm tin vào tiến độ, tôi bị nghi làm thất lạc, và việc nhập hồ sơ bị ngắt quãng mỗi lần bị hỏi |
| Success metric (baseline → target) |Thời gian trả lời từ 2-3 phút xuống dưới 1 phút/lần hỏi; thất lạc từ 2-3 lần/tháng xuống tối đa 1 lần/tháng |
| Phương án không dùng AI |Sổ hoặc bảng trạng thái (đã nhận / đã nhập / thiếu) có ngày nhận, giáo viên tự xem. Giải quyết phần lớn nếu được cập nhật đều, nhưng tôi phải nhớ ghi mỗi lần nhận hồ sơ |
| Giả thuyết về AI (nếu có) |AI trả lời câu hỏi “hồ sơ của X đang ở đâu” dựa trên dữ liệu đã nhập; tôi chỉ xác nhận lại những trường hợp AI không chắc |
| Cảm nhận nhanh | Chưa biết |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 2-3 phút/lần hỏi

[1 Nhận câu hỏi] → [2 Tìm hồ sơ ở nhiều chỗ] ← BOTTLENECK
→ [3 Xác định đã nhập chưa] → [4 Trả lời giáo viên]
```

### Card muốn pitch nhất

- Card số: 1
- Vì sao: Việc chiếm nhiều thời gian nhất trong tuần, actor rõ, bottleneck là một bước cụ thể và đo được bằng phút/hồ sơ. Card 2 và 3 phần lớn là hậu quả của việc nhập chậm hoặc hồ sơ thiếu.
- Câu hỏi muốn nhóm phản biện: Nếu AI điền sẵn mà tôi vẫn phải kiểm tra từng hồ sơ, thời gian kiểm tra có ăn hết phần tiết kiệm không? Và nếu giáo viên chỉ cần nộp theo form chuẩn thì có cần AI nữa không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
|Target 2 phút/hồ sơ không có cơ sở, kiểm tra bản nháp cũng tốn thời gian  |Đồng ý  | Đổi target thành 3 phút/hồ sơ, chỉ áp dụng cho hồ sơ rõ nét |
| Form chuẩn, Excel có thể đã đủ, chưa nói vì sao cần AI | Đồng ý |Thêm lý do: form không giải được hồ sơ giấy và ảnh chụp, vẫn phải gõ lại  |
|Thiếu rủi ro: hồ sơ chứa thông tin cá nhân |Đồng ý | Thêm điều kiện: che CCCD, địa chỉ và xin phép trung tâm trước khi thử|

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: với candidate “Theo kịp group chat sau thời gian nghỉ” của Huy, tôi cùng Đức phản biện rằng thời gian nghỉ phép không nhiều nên candidate này không có quá nhiều giá trị |Candidate này không được nhóm chọn. |
| Nhận phản biện | Câu hỏi tôi nhận được: (1) thời gian chờ hồ sơ cứng có dài hơn thời gian gõ không, form chuẩn có giảm bước gõ không; (2) trung tâm từng có danh sách giấy tờ bắt buộc chưa; (3) hệ thống có biết hồ sơ đã nhập chưa| Tôi đã sửa gì: ở Card #1, tách thời gian chờ ra khỏi bottleneck, thêm lý do form chuẩn chưa giải quyết được hồ sơ giấy, đổi target thận trọng hơn (6' → 3'/hồ sơ), thêm điều kiện che dữ liệu cá nhân|
| Gom cluster / cây OST |Gom 12 candidate (mỗi bạn 3) thành 4 cluster (nhập/phân loại, đối soát, tổng hợp họp/chat, tra cứu trạng thái); viết cây OST gồm 1 outcome và 4 opportunity; gạch 6 ý là solution đội lốt opportunity |Nhóm có cluster và cây OST làm cơ sở chọn candidate |
| Chọn candidate problem |Candidate được chọn: Candidate #1: Phân loại phản hồi / ticket khiếu nại từ khách hàng để điều phối cho đội kỹ thuật và sản phẩm. | cả nhóm đều chọn candidate 1 |
| Kiểm chứng / research | | |
| Quy trình nhóm |Viết Problem Statement v0 (6 trường); nhờ AI chỉ lỗ hổng | Quy trình giảm từ 5 xuống 4 bước, thời gian từ 45' xuống dưới 10' (kỳ vọng), bottleneck chuyển sang bước người kiểm tra.|
| Problem Statement | nhờ AI chỉ lỗ hổng| Phản biện chỉ ra metric chưa đo độ đúng và baseline là ước lượng; nhóm thêm metric chất lượng ở v1, ghi rõ baseline là ước lượng, bổ sung điều kiện xin phép khi ghi âm|
| Mức can thiệp AI | Theo mức workflow | vẫn cần con người phải kiểm tra lần cuối |
| Quyết định | Kết luận chưa đủ | cần phải kiểm chứng thêm |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan |Có nhờ AI để gợi ý tưởng | Liệt kê ra các ý tưởng nhanh chóng | Không có | Tôi không áp dụng được gì từ các gợi ý AI |
| CP2 Problem Card |nhờ AI hỗ trợ và phản biện các problem card |AI đưa ra những điểm sai cần cải thiện |không có | Tôi áp dụng và chỉnh sửa các ý mà AI cho là sai |
| CP4 Research | hỗ trợ team trong quá trình hoàn thành phần 4 | gợi ý AI đưa ra có vẻ hợp lý |không có | dựa vào những gọi ý AI đưa ra để hoàn thành |
| CP5 Quy trình |có nhờ AI hỗ trợ gợi ý sơ đồ ý tưởng |AI gợi ý ý tưởng khá hay |không có |dựa vào gợi ý của AI trong quá trình hoàn thành |
| CP5–6 Problem Statement | Nhờ AI chỉ ra lỗ hổng, chỗ sai sau khi viết |AI chỉ ra metrics chưa đo độ đúng |không có | bổ sung điều kiện xin phép trước khi ghi âm |
| CP6 Mức can thiệp / quyết định | nhờ AI thử can thiệp vào hỗ trợ | AI có vẻ khá nhanh trong hỗ trợ công việc | vẫn có tỉ lệ khả năng AI sai sót | vẫn cần phải để con người kiểm tra lần nữa trước khi chốt |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Nghe bài toán đối soát của Đức, hóa đơn của Duẩn và phân loại feedback của Huy, tôi nhận ra điểm mấu chốt là phải xác định đúng bottleneck định lượng. Vấn đề thực sự đáng giải cần có quy trình rõ ràng và đo được bằng thời gian hay tỷ lệ lỗi cụ thể, chứ không chỉ dựa vào cảm giác quá tải hay than phiền chủ quan.
**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
Nhóm hiện tại chưa bị "Solution-first", nhóm luôn lắng nghe các thành viên giải thích về vấn đề trước khi đưa ra giải pháp
**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Tôi có. Ban đầu tôi nghĩ AI sẽ giải quyết triệt để việc nhập 150 hồ sơ/tuần. Khi bị nhóm phản biện gắt câu hỏi: "Nếu thời gian chờ hồ sơ giấy còn lâu hơn thời gian gõ thì AI giải quyết được gì?", tôi nhận ra AI chỉ giải quyết được phần ngọn (bước gõ), bởi vậy nên tôi mới quyết định giới hạn lại.
**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
Tôi cũng không bất ngờ lắm vì thường các giáo viên sẽ luôn được yêu cầu mang những gì để nộp hồ sơ để nhập danh sách học viên, việc mang thiếu là do họ chưa có giấy tờ tương ứng hoặc đang đi làm lại
**6.5. Điều khó nhất khi viết Problem Statement là gì?**
Khó nhất là kiềm chế không gài sẵn chữ "cần AI" vào câu mô tả vấn đề, và phải bấm giờ thực tế từng bộ hồ sơ để lấy baseline chuẩn (khoảng 3 phút/bộ) thay vì phỏng đoán theo cảm tính bực bội hằng ngày
**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Tôi sẽ bấm giờ thực tế sớm hơn và phản biện nhóm mạnh mẽ: "Đừng vội tính đến AI khi quy trình đầu vào còn chưa có checklist chuẩn!". Tự động hóa trên một quy trình vốn còn lộn xộn sẽ không giải quyết được gốc rễ vấn đề
**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
