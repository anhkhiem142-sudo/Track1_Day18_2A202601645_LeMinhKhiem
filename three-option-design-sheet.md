# Three-Option Design Sheet — Case A: AI Tutor

## Hypothesis Problem (mang từ Chặng 1, Day 18)

> Khi đang học và gặp một phần nội dung chưa hiểu (vì thiếu nghĩa thuật ngữ, thiếu giải thích tại chỗ, hoặc giảng viên đi nhanh), learner khó tiếp tục theo kịp bài giảng vì không có cách xử lý vướng mắc ngay tại chỗ mà không phải rời luồng học để tự tra cứu (chatbot nội bộ, Google, AI ngoài) — dẫn đến bỏ lỡ nội dung tiếp theo, dồn nợ kiến thức và mất mạch bài giảng.

*Đối với Hypothesis Problem, chúng tôi đã đổi từ problem gốc Day 17 ("thiếu kiến thức nền") sau khi đối chiếu 3 Practice Notes: root cause cụ thể khác nhau ở mỗi người (từ vựng / slide thiếu giải thích / tốc độ giảng nhanh), nhưng cấu trúc barrier + consequence giống nhau 3/3 lần — nên trọng tâm chuyển sang "thiếu kênh xử lý tại chỗ, không rời luồng".*

## Content fixture dùng chung (~70%)

- **Target user:** Learner đang học trên VLearn
- **Situation:** Đang xem slide bài học, gặp một khái niệm không có giải thích kèm theo
- **Task:** Dùng phương án để tiếp tục hiểu bài mà không bị mất mạch học
- **Desired outcome:** Hiểu đủ để tiếp tục theo kịp phần sau
- **Content/data fixture:** Slide "MVE, MVP, PoC: Khác Nhau Ở Mục Tiêu" — bảng so sánh 3 khái niệm product management, không có định nghĩa kèm theo trên slide

## Ba Solution Options — phần được phép khác

| Thành phần | Option A — Highlight-to-ask | Option B — Sổ tay tĩnh | Option C — AI chủ động phát hiện |
|---|---|---|---|
| **Solution mechanism** | Bôi đen thuật ngữ (MVE/MVP/PoC) → AI hỏi 1 câu chẩn đoán ("đã từng nghe chưa?") → chọn mức giải thích phù hợp (ngắn/đầy đủ) → có ô chat để hỏi thêm | Nút "Sổ tay bài học" cố định → mở drawer chứa toàn bộ định nghĩa viết sẵn cho cả 3 thuật ngữ | Theo dõi thời gian learner ở lại slide (dwell time) → sau 15 giây không tương tác, chủ động hiện bubble đề xuất giải thích |
| **User làm gì?** | Chủ động bôi đen đúng thuật ngữ, trả lời câu hỏi chẩn đoán, có thể gõ hỏi thêm | Chủ động tìm và bấm nút, tự tìm đúng mục trong danh sách | Chỉ cần đọc bình thường; khi bubble hiện thì chọn Xem hoặc Không |
| **AI làm gì?** | **Act** — đặt câu hỏi chẩn đoán, chọn mức giải thích, trả lời câu hỏi mở rộng | **Don't Act** — chỉ retrieve nội dung tĩnh, không suy luận | **Ask** — chủ động đề xuất dựa trên tín hiệu dwell time, không tự chèn nội dung nếu bị từ chối |
| **Trigger** | User bôi đen text | User bấm nút sổ tay | Dwell time ≥ 15 giây không tương tác |
| **Trade-off chính** | Cá nhân hoá theo mức đã biết, nhưng có thêm 1 bước hỏi trước khi thấy câu trả lời | Nhanh, không rủi ro sai, nhưng không neo vào đúng từ đang gây khó — user phải tự tìm trong danh sách | Không cần user tự nhận ra vướng mắc, nhưng có rủi ro false positive (đọc chậm tự nhiên ≠ đang bối rối) |

### Distance check

**A khác B vì:** A có bước AI suy luận/chẩn đoán trước khi trả lời; B chỉ tra cứu nội dung tĩnh, không có suy luận nào.

**B khác C vì:** B đòi hỏi user chủ động tự tìm và mở sổ tay; C để AI tự phát hiện và đề xuất mà user không cần làm gì trước.

**A khác C vì:** A chỉ Act sau khi user chủ động chọn văn bản để hỏi; C chủ động Ask dựa trên tín hiệu hành vi, không cần user thao tác gì trước.

## Human–AI Decision Table (Chặng 3)

| Human–AI decision | Option A | Option B | Option C |
|---|---|---|---|
| **User làm gì? AI làm gì?** | User bôi đen thuật ngữ → AI hỏi chẩn đoán → chọn mức giải thích → generate câu trả lời | User bấm nút → hệ thống hiện đúng nội dung tĩnh đã viết sẵn | AI quan sát dwell time → chủ động đề xuất; user chấp nhận hoặc từ chối |
| **AI Act / Ask / Don't Act? Vì sao?** | **Act** — tự sinh câu trả lời sau khi có 1 tín hiệu chẩn đoán, rủi ro nếu chẩn đoán sai | **Don't Act** — chỉ lookup, không suy luận, rủi ro sai gần như 0 | **Ask** — không áp đặt, nhưng có rủi ro làm phiền nếu tín hiệu (dwell time) không phản ánh đúng trạng thái bối rối |
| **User hiểu capability/limit bằng gì?** | Card "Trước khi giải thích..." nói rõ AI sẽ hỏi 1 câu trước | Nhãn ngầm định "sổ tay" gợi ý đây là tra cứu tĩnh, không phải AI | Chưa có thông báo trước về việc hệ thống theo dõi thời gian — **đây là điểm cần bổ sung trước khi test thật** (xem Still Unproven) |
| **Evidence/uncertainty thể hiện thế nào?** | Evidence tag: "Dựa trên câu trả lời vừa rồi — bạn đã quen/lần đầu gặp thuật ngữ này" | Không cần — nội dung tĩnh | Evidence tag: "Vì bạn đã ở lại slide này hơn 15 giây" |
| **User kiểm soát và recovery thế nào?** | Đóng modal bất kỳ lúc nào; có thể tiếp tục hỏi qua chat | Đóng drawer bằng nút X bất kỳ lúc nào | Nút "Không, cảm ơn" luôn có; sau khi từ chối, không hỏi lại về cùng nội dung trong phiên đó |

## Solution Parking Lot (Các option còn lại từ Day 17)

| # | Hướng | AI / Không AI |
|---|---|---|
| 3 | Prerequisite check trước khi vào bài | AI |
| 5 | Nút kết nối nhanh tới bạn học đang online / thread hỏi-đáp | Không AI |
