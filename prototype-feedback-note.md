# Prototype Feedback Note — Lê Minh Khiêm

**Tester/context:** TESTER_003, là một học viên trong khóa Đào tạo nhân tài AI thực chiến.

| Observation | Note |
|---|---|
| First action | Bấm được ngay vào mục "Sổ tay bài học" đối với option B, bối rối không biết làm gì khi ở option A và C |
| Chỗ dừng, do dự hoặc hiểu sai | Option A không biết bôi đen ở đâu. Option C không biết phải làm gì để được hỗ trợ |
| Evidence được đọc hay bỏ qua | Evidence được đọc |
| Cách tester sửa hoặc lấy lại control | Bôi đen nhiều chỗ và cuối cùng thì trúng vào chính xác khái niệm |
| Option được chọn | **B** — tester nói rõ: "mình thích giao diện này nhất, có vẻ khá tiện lợi" |
| Lý do và trade-off | **Option A:** "mình muốn bôi đen thì AI sẽ hiện ra luôn giải thích chứ không phải để mình xác nhận qua bước hỏi trước". **Option B:** "mình thích giao diện này nhất, có vẻ khá tiện lợi". **Option C:** "liệu mình có bị làm phiền nếu nó cứ hiện ra như vậy không" |
| Evidence chống lại kỳ vọng của nhóm | Bước chẩn đoán ở Option A được thiết kế có chủ đích (đúng solution directive gốc — AI chẩn đoán trước khi giải thích), nhưng tester coi đây là bước thừa gây chậm trải nghiệm — mâu thuẫn trực tiếp với giả định thiết kế ban đầu |

## Tách bốn lớp

**OBSERVED** — Tester đã làm hoặc nói gì?
> Về Option A: muốn AI hiện giải thích ngay khi bôi đen, không cần bước hỏi/xác nhận trước. Về Option B: nói đây là giao diện thích nhất, thấy tiện lợi. Về Option C: đặt câu hỏi lo ngại về việc bị làm phiền nếu bubble cứ tự động hiện ra.

**INTERPRETED** — Nhóm nghĩ điều đó có thể có nghĩa gì?
> Tester này ưu tiên tốc độ/ít bước hơn cá nhân hoá — bước chẩn đoán của A, dù có giá trị thiết kế, bị coi là friction chứ không phải tính năng. Lựa chọn rõ ràng cho B củng cố tín hiệu "tốc độ thắng" đã thấy ở tester khác. Concern về C cho thấy AI chủ động cần cân nhắc tần suất, không chỉ nội dung đề xuất.

**DECIDED — NEXT CHANGE**
> Chốt chung ở [`group-feedback-synthesis.md`](group-feedback-synthesis.md).

**STILL UNPROVEN** — Điều gì chưa thể kết luận từ một người?
> Không rõ nếu bỏ bước chẩn đoán ở A, chất lượng/độ liên quan của giải thích có giảm không (trade-off giữa tốc độ và cá nhân hoá) — cần test riêng để so sánh.
