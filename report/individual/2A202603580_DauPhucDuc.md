# Báo cáo cá nhân — 2A202603580_Đậu Phúc Đức



## 1. Thông tin học viên

- Họ tên: Đậu Phúc Đức
- MSSV: 2A202603580
- Email trường (không bắt buộc, repo có thể để public): 
- Tên nhóm: XYZ
- Link repo nhóm: https://github.com/dpduc/K5-L3-Day02-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

Bối cảnh: Chị Mai làm kế toán, chị thường xuyên phải thực hiện đối soát thông tin (sao kê ngân hàng, file settlement cổng thanh toán, hóa đơn, công nợ) với sổ sách kế toán và hệ thống bán hàng ở một doanh nghiệp bán hàng đa kênh.


| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật: thời gian làm thủ công (ước lượng) | Cách đo |
|---:|---|---|---|---|---|
| 1.1 | Lặp lại | Khi nhận file settlement hằng ngày từ nhiều cổng thanh toán, chị Mai muốn khớp từng giao dịch với đơn trên hệ thống bán hàng, để phát hiện đơn đã thu tiền nhưng chưa ghi nhận, hoặc đã ghi nhận nhưng tiền chưa về | Kế toán thanh toán | Hằng ngày, 60 phút/ngày (~20 giờ/tháng): tải file từng cổng, VLOOKUP theo mã đơn, lọc dòng lệch | Số giao dịch lệch mỗi ngày; số phút đối soát mỗi ngày |
| 1.2 | Lặp lại | Khi khách chuyển khoản với nội dung không chuẩn (sai mã đơn, chỉ ghi tên, gộp nhiều đơn), chị Mai muốn xác định khoản tiền thuộc đơn hoặc khách nào, để gạch công nợ đúng | Kế toán công nợ | 5-10 phút/khoản; ~5–8 khoản/ngày -> 50–100 phút/ngày (tra tên, SĐT, lịch sử đơn, hỏi sales) | Số khoản tiền treo chưa xác định; số ngày trung bình một khoản bị treo |
| 1.3 | Lặp lại | Khi đơn vị vận chuyển trả tiền COD theo đợt, Mai muốn đối chiếu số tiền về với danh sách đơn giao thành công sau khi trừ phí ship và phí hoàn, để biết đợt đó thiếu tiền ở đơn nào | Kế toán | 45–90 phút/đợt, 2–3 đợt/tuần -> 2–4 giờ/tuần (ghép bảng kê COD với đơn giao thành công, tính lại phí từng đơn) | Chênh lệch COD mỗi đợt; số đơn thiếu tiền; số đơn bị thu phí sai |
| 1.4 | Lặp lại | Khi sàn TMĐT thanh toán theo kỳ và đã trừ sẵn nhiều loại phí (hoa hồng, voucher, phí vận chuyển, phí dịch vụ), Mai muốn tách số tiền theo từng loại phí, để hạch toán đúng tài khoản chi phí | Kế toán tổng hợp | 2–3 giờ/kỳ/sàn; 2–3 sàn, 2–4 kỳ/tháng → 8–20 giờ/tháng (đọc báo cáo doanh thu của sàn, pivot theo loại phí, lập bút toán) | Tỷ lệ số tiền chưa phân loại được; thời gian hạch toán một kỳ thanh toán |
| 1.5 | Lặp lại | Khi nhận hóa đơn đầu vào từ nhà cung cấp, Mai muốn đối chiếu hóa đơn với đơn mua hàng và phiếu nhập kho, để không thanh toán sai số lượng hoặc đơn giá | Kế toán mua hàng | 5–10 phút/hóa đơn; ~150 hóa đơn/tháng → 12–25 giờ/tháng | Số hóa đơn lệch mỗi tháng; số tiền thanh toán sai phát hiện sau khi đã trả |
| 2.1 | Tốn thời gian | Khi khóa sổ cuối tháng, Mai muốn biết khoản nào còn lệch giữa sổ cái và sao kê ngân hàng, để không phải kéo dài thời gian khóa sổ | Kế toán trưởng | 1–2 ngày công/tháng rà lệch; khóa sổ thường mất 5–7 ngày làm việc sau cuối tháng | Số ngày làm việc từ cuối tháng đến khi khóa sổ; số khoản lệch còn mở lúc khóa sổ |
| 2.2 | Tốn thời gian | Khi doanh thu trên hệ thống bán hàng khác doanh thu trên sổ kế toán, Mai muốn truy ra nguyên nhân (hủy đơn, hoàn tiền, đổi trả, lệch ngày ghi nhận), để giải trình được phần chênh lệch | Kế toán, giám đốc | 30–60 phút/khoản lệch; ~1–2 ngày công/tháng | Thời gian truy một khoản lệch; tỷ lệ chênh lệch giải thích được |
| 2.3 | Tốn thời gian | Khi đơn bị hoàn tiền sau khi đã xuất hóa đơn, Mai muốn biết đơn nào chưa được lập hóa đơn điều chỉnh hoặc thay thế, để tránh sai sót về thuế | Kế toán thuế | 5–10 phút/đơn hoàn; ~4–6 giờ/tháng (lọc đơn hoàn, tra từng hóa đơn trên hệ thống HĐĐT) | Số đơn hoàn tiền chưa xử lý hóa đơn quá X ngày |
| 2.4 | Tốn thời gian | Khi xuất hóa đơn điện tử cho đơn bán lẻ từ nhiều kênh, Mai muốn biết đơn nào chưa xuất hoặc bị xuất trùng, để không sót doanh thu và không xuất hai lần | Kế toán | 30–60 phút/ngày (~10–20 giờ/tháng): xuất danh sách đơn từng kênh, ghép với danh sách hóa đơn đã phát hành | Số đơn chưa xuất hóa đơn; số hóa đơn trùng mỗi tháng |
| 3.1 | Cần đọc, tổng hợp nhiều thông tin | Khi đọc hợp đồng với sàn, cổng thanh toán hoặc đơn vị vận chuyển, Mai muốn nắm mức phí, chu kỳ thanh toán và điều khoản phạt đã cam kết, để kiểm tra đối tác có thu đúng không | Trợ lý giám đốc, kế toán | 1–2 giờ/hợp đồng (5–10 hợp đồng); sau đó 2–3 giờ/tháng so phí thực thu với phí cam kết | Số khoản phí thu sai phát hiện được và tổng số tiền |
| 3.2 | Cần đọc, tổng hợp nhiều thông tin | Khi sàn thông báo thay đổi chính sách phí, Mai muốn ước tính thay đổi đó làm biên lợi nhuận theo kênh hoặc nhóm sản phẩm tăng giảm bao nhiêu, để báo sếp trước khi áp dụng | Giám đốc | 0,5–1 ngày công/lần thay đổi, vài lần/quý (đọc thông báo, lấy doanh số theo nhóm sản phẩm, dựng lại bảng tính biên lợi nhuận) | Thời gian từ lúc có thông báo đến lúc có con số ước tính |
| 3.3 | Cần đọc, tổng hợp nhiều thông tin | Khi lập báo cáo tuổi nợ phải thu, Mai muốn gom số dư từ nhiều nguồn (sàn, đại lý, khách B2B, COD đang giữ ở đơn vị vận chuyển), để biết ai đang nợ quá hạn và nợ bao nhiêu | Kế toán công nợ, giám đốc | 4–6 giờ/lần, mỗi tháng (gom tay từ 4+ nguồn rồi chia nhóm tuổi nợ) | Số nguồn phải gom tay; độ trễ của báo cáo so với ngày chốt số liệu |
| 3.4 | Cần đọc, tổng hợp nhiều thông tin | Khi tiền quảng cáo bị trừ qua thẻ (Facebook, Google, quảng cáo trên sàn), Mai muốn đối chiếu số tiền bị trừ với hóa đơn hoặc biên lai tương ứng, để chứng từ chi phí đầy đủ | Kế toán | 3–5 giờ/tháng (tải biên lai từng nền tảng, khớp với sao kê thẻ, quy đổi ngoại tệ) | Số khoản chi thiếu chứng từ; số tiền chi phí không được khấu trừ |
| 3.5 | Cần đọc, tổng hợp nhiều thông tin | Khi sếp chuẩn bị họp với ngân hàng hoặc nhà đầu tư, Mai muốn tổng hợp dòng tiền thực thu và thực chi theo kênh trong kỳ, để sếp trả lời được các câu hỏi về số liệu | Giám đốc | 1–2 ngày công/lần, vài lần/năm | Thời gian chuẩn bị; số lần phải sửa số sau khi đã gửi |
| 4.1 | Pain từ người khác | Khi sếp hỏi bất chợt "hôm nay tiền về bao nhiêu, tài khoản còn bao nhiêu", Mai muốn trả lời bằng số đã đối soát, để sếp quyết định chi hoặc duyệt thanh toán ngay | Giám đốc | 15–30 phút/lần, 3–5 lần/tuần (vào từng tài khoản ngân hàng, cộng tiền về, trừ khoản chưa đối soát) | Thời gian từ lúc sếp hỏi đến lúc có câu trả lời; số lần trả lời xong phải đính chính |
| 4.2 | Pain từ người khác | Khi khách khiếu nại đã chuyển khoản mà đơn chưa được xác nhận, nhân viên CSKH muốn biết tiền đã về chưa, để trả lời khách mà không phải chờ kế toán | CSKH, sales | Kế toán mất 5–10 phút/yêu cầu; CSKH chờ 30–120 phút; ~20–40 yêu cầu/tuần | Số yêu cầu kiểm tra gửi sang kế toán mỗi tuần; thời gian chờ phản hồi |
| 4.3 | Pain từ người khác | Khi đơn bị hoàn, kho và kế toán muốn thống nhất trạng thái của đơn (kho đã nhận hàng hoàn chưa, sàn hoặc khách đã được hoàn tiền chưa), để không mất hàng hoặc mất tiền | Thủ kho, kế toán | 2–3 giờ/tuần (đối chiếu sổ hàng hoàn của kho với danh sách hoàn tiền) | Số đơn lệch trạng thái giữa kho và kế toán; giá trị hàng hoàn chưa xác nhận |
| 4.4 | Pain từ người khác | Khi nhà cung cấp hỏi bao giờ được thanh toán, kế toán muốn biết hóa đơn của họ đang ở bước nào (chờ đối chiếu, chờ duyệt, đã lên lịch chi), để trả lời chính xác | Nhà cung cấp, kế toán mua hàng | 10–15 phút/lần tra (email, file theo dõi, hỏi người duyệt); ~10 lần/tuần | Số lần nhà cung cấp phải nhắc; số khoản thanh toán trễ hạn |
| 4.5 | Pain từ người khác | Khi kiểm toán hoặc cơ quan thuế yêu cầu giải trình một bút toán, tôi muốn tìm ra chứng từ gốc và các giao dịch liên quan, để giải trình đúng hạn | Kế toán trưởng, kiểm toán viên | 30–60 phút/bút toán; mùa kiểm toán 30–50 yêu cầu → 15–50 giờ | Thời gian tìm đủ chứng từ cho một bút toán; số yêu cầu bị trễ hạn |
| 4.6 | Pain từ người khác | Khi marketing báo cáo hiệu quả quảng cáo theo số liệu của nền tảng, sếp muốn biết doanh thu thực thu sau khi trừ hủy, hoàn và phí, để đánh giá kênh nào thực sự có lãi | Giám đốc, marketing | 3–5 giờ/tháng (ghép doanh thu theo kênh với dữ liệu hủy, hoàn, phí) | Chênh lệch giữa doanh thu marketing báo cáo và doanh thu thực thu theo kênh |

> Thời gian ở cột "Dấu hiệu thật" là ước lượng dựa trên trải nghiệm thật và có tính chủ quan. 

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

-

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Đối soát tiền cổng thanh toán | Đây là task tốn nhiều thời gian và mang tính lặp lại nhất của Mai | Cổng thanh toán hoặc OMS có sẵn tính năng đối soát chưa? Nếu có mà chưa dùng, vấn đề là quy trình, không phải công cụ. |
| 2 | Xử lý tiền chuyển khoản treo | Pain lan sang người khác: CSKH chờ xác nhận, khách chờ đơn, sales bị hỏi. Lợi ích vì thế không chỉ là giờ làm của M. | Success metric và baseline |
| 3 | Trả lời sếp về tình hình tiền | Mỗi lần trả lời chậm hoặc phải đính chính có thể làm chậm quyết định chi của sếp | Budget AI API |

### Problem Card #1 - Đối soát tiền từ cổng thanh toán

| Trường | Nội dung |
|---|---|
| Job Story | Khi nhận file settlement buổi sáng từ các cổng thanh toán, Mai muốn biết giao dịch nào chưa khớp với đơn trên hệ thống bán hàng, để xử lý lệch trước khi ghi sổ doanh thu trong ngày|
| Actor | Mai - báo cáo kế toán trưởng, CEO |
| Thời điểm / bối cảnh | 9h–10h sáng mỗi ngày làm việc, sau khi các cổng gửi file của ngày hôm trước |
| Quy trình hiện tại (3–7 bước) |1. Tải file settlement từ từng cổng · 2. Export đơn thanh toán online từ OMS · 3. Chuẩn hóa cột (mã đơn, số tiền, phí, ngày) · 4. VLOOKUP theo mã đơn · 5. Rà từng dòng lệch, tra lại trên portal cổng và OMS · 6. Ghi nguyên nhân, lập danh sách lệch · 7. Gửi kế toán trưởng |
| Bottleneck (bước nào, mất bao nhiêu phút) |Bước 5, rà dòng lệch: khoảng 25 phút. Mỗi dòng phải mở 2 hệ thống, dù nguyên nhân thường lặp lại (hoàn một phần, đơn tách, lệch ngày) |
| Impact (nếu không giải thì sao) | Khoảng 80 phút/ngày, tức 6,5 giờ/tuần. Khoản lệch chưa xử lý dồn đến cuối tháng làm chậm khóa sổ |
| Success metric (baseline → target) |Tổng thời gian dưới 25 phút/ngày; 100% dòng lệch được phân loại nguyên nhân trong ngày; không còn khoản lệch tồn quá 3 ngày |
| Phương án không dùng AI |Power Query chuẩn hóa và khớp tự động, kèm bảng mã nguyên nhân thường gặp. Bước 3–4 gần như hết; bước 5 giảm được phần lệch có quy luật |
| Giả thuyết về AI (nếu có) |AI đề xuất nguyên nhân cho dòng lệch dựa trên các ca đã xử lý trước đó; M xác nhận hoặc sửa |
| Cảm nhận nhanh | Automation trước, AI sau. Phần lớn là rule-based |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 80 phút/ngày

[1 Tải settlement: 10'] → [2 Export OMS: 5'] → [3 Chuẩn hóa cột: 15']
→ [4 VLOOKUP: 10'] → [5 Rà dòng lệch: 25'] ← BOTTLENECK
→ [6 Ghi nguyên nhân: 10'] → [7 Gửi: 5']
```

### Problem Card #2 - Tiền chuyển khoản treo

| Trường | Nội dung |
|---|---|
| Job Story |Khi sao kê có khoản tiền vào với nội dung chuyển khoản không chuẩn, tôi muốn xác định khoản đó thuộc đơn hoặc khách nào, để gạch công nợ và xác nhận đơn đúng |
| Actor | Mai -> CSKH, sales |
| Thời điểm / bối cảnh | Theo kỳ thanh toán của từng sàn (hằng tuần), dồn nhiều vào cuối tháng |
| Quy trình hiện tại (3–7 bước) | 1. Tải báo cáo từ từng sàn · 2. Mở file, mỗi sàn một cấu trúc cột khác nhau · 3. Map tên phí của sàn sang tài khoản kế toán · 4. Cộng theo loại phí, kiểm tổng có khớp tiền về không · 5. Lập bút toán · 6. Lưu file đối chiếu |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, map tên phí: khoảng 25 phút. Sàn đổi tên phí hoặc thêm phí mới theo chính sách, không có quy tắc sẵn |
| Impact (nếu không giải thì sao) | Khoảng 75 phút/kỳ. Phí không rõ bị dồn vào “chi phí khác”, nên biên lợi nhuận theo kênh bị sai |
| Success metric (baseline → target) | Dưới 25 phút/kỳ; số tiền chưa phân loại dưới 2% tổng phí |
| Phương án không dùng AI | Bảng mapping tên phí sang tài khoản cho từng sàn, cập nhật khi có phí mới, kết hợp Power Query cho từng sàn |
| Giả thuyết về AI (nếu có) | AI chỉ xử lý ngoại lệ: đề xuất tài khoản cho dòng phí mới chưa có trong bảng mapping, kèm lý do; kế toán duyệt rồi bổ sung vào bảng |
| Cảm nhận nhanh | Workflow, AI xử lý ngoại lệ |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 75 phút/kỳ

[1 Tải báo cáo sàn: 10'] → [2 Đọc cấu trúc file: 5']
→ [3 Map phí → tài khoản: 25'] ← BOTTLENECK
→ [4 Cộng + kiểm tổng: 15'] → [5 Lập bút toán: 15'] → [6 Lưu file: 5']
```

### Problem Card #3 - Trả lời sếp về tình hình tiền

| Trường | Nội dung |
|---|---|
| Job Story | Khi sếp hỏi “hôm nay tiền về bao nhiêu, còn bao nhiêu”, Mai muốn trả lời bằng số đã đối soát trong vài phút, để sếp quyết định duyệt chi ngay |
| Actor | CEO, Mai |
| Thời điểm / bối cảnh | Bất chợt, thường trước khi duyệt thanh toán cho nhà cung cấp hoặc ngay trong cuộc họp |
| Quy trình hiện tại (3–7 bước) | 1. Đăng nhập internet banking từng tài khoản · 2. Xem số dư và giao dịch trong ngày · 3. Kiểm tra tiền đang chờ về từ cổng, sàn, COD · 4. Trừ các khoản chi đã duyệt nhưng chưa thanh toán · 5. Tổng hợp và nhắn sếp |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, tiền đang chờ về: khoảng 15 phút. Số liệu nằm rải rác ở nhiều portal |
| Impact (nếu không giải thì sao) | Khoảng 45 phút/lần, chừng 3 lần/tuần. Việc khác bị ngắt quãng; đôi khi gửi số sơ bộ rồi phải đính chính |
| Success metric (baseline → target) | Thời gian trả lời dưới 5 phút; không phải đính chính lần nào |
| Phương án không dùng AI | Bảng dòng tiền cập nhật cuối mỗi ngày, lấy kết quả từ card #1, #2; sếp xem trực tiếp |
| Giả thuyết về AI (nếu có) | Sếp hỏi bằng câu tự nhiên, AI trả lời từ bảng dòng tiền đã đối soát và ghi rõ nguồn của từng con số |
| Cảm nhận nhanh | AI |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 30 phút/lần

[1 Xác định khoảng thời gian đối soát và pull dữ liệu: 10'] → [2 Xác định trường tính toán và phép tính: 10']
 ← BOTTLENECK
→ [3. Soạn báo cáo: 5-10']
```

### Card muốn pitch nhất

- Card số: #1
- Vì sao: Đây là task tốn thời gian và lặp đi lặp lại nhất của Mai
- Câu hỏi muốn nhóm phản biện: Sai số / mức độ automation của AI có đáng để người dùng trả tiền chưa? 

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Giá trị của AI phần lớn nằm ở lượng thời gian tiết kiệm được. Giờ tiết kiệm khó quy ra tiền và chất lượng công việc | Một phần | đây không hẳn là điểm yếu, thời gian tiết kiệm được là giá trị thật. Giữ nguyên quan điểm về tiềm năng tích hợp AI. |


---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Pitch và phản biện các câu hỏi đưa ra cả 3 Problem Card | Nhận được góp ý cải thiện metrics đánh giá |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Sản phẩm của H là gì - khách hàng là ai, có bao nhiêu unique expected tickets cho 1 ticket, AI hỗ trợ phân loại tới đâu | Giúp H xác định scope |
| Nhận phản biện | Câu hỏi tôi nhận được: Quy trình đối soát ngày nay đã được tự động hóa tới mức độ nào? Các công cụ hõ trợ đối soát tiên phong đang làm ntn? | Tôi đã sửa gì: bổ sung metrics |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Viết lại vấn đề, đề xuất các vấn đề tương tự, tranh biện | Khả năng đề xuất vấn đề tương tự, tranh biện phản biện trên chính quan điểm trước đó của nó | đánh giá quá thấp khả năng làm việc thủ công của con người | tiềm năng tự động hóa và goal của bài toán |
| CP2 Problem Card | Viết problem card, phản biện | hữu ích - task và scope đã rõ | hữu ích | không sửa |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
- Cách tiếp cận và định nghĩa vấn đề


**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
- Có. Hỏi lại - vấn đề đang được giải quyết là gì? 

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
- Không. Quá trình phản biện giúp tôi định nghĩa vấn đề chính xác hơn. 

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
- Không. Ý kiến khác nhau là bình thường. 

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
- Xác định chính xác vấn đề và scope của giải pháp

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
- Dùng AI nhiều hơn trong lúc làm bài @@ - quá trình phản biện với người chỉ hiệu quả khi nhóm đã có 1 mục tiêu chung và hiểu cách làm việc của nhau

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.


---

## 7. Tài liệu tham khảo

-
