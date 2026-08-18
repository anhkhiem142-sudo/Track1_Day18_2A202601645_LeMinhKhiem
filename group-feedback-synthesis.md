# Group Feedback Synthesis

| Nội dung | Feedback 1 (tester — Vân) | Feedback 2 (tester — Khiêm) | Feedback 3 (tester — Tuyết) | Pattern hoặc khác biệt |
|---|---|---|---|---|
| First action | Với option A, bạn đang đọc qua và bôi đen "đoạn văn" bạn đang thắc mắc. Với option B, bạn đọc lướt qua và bấm vào "Sổ tay bài học". Với option C, bạn scroll qua lại | Bấm được ngay vào mục "Sổ tay bài học" đối với option B, bối rối không biết làm gì khi ở option A và C | Bôi đen nhiều đoạn văn bản (Option A). Bấm vào "Sổ tay bài học" (Option B). Scroll qua lại trang slide (Option C) | Với option B, các tester đều có thể dễ dàng chọn ngay vào "Sổ tay bài học", tuy nhiên với option B và C user đều khá bối rối trước khi thực sự chạm được vào tính năng mà nhóm phát triển nếu không có thời gian sử dụng dài hoặc có sự hướng dẫn từ trước đó |
| Breakdown chính (Option A) | "Muốn biết rõ khái niệm nào được AI hỗ trợ — cần highlight/gạch dưới để biết bấm vào đâu" | "Muốn bôi đen là AI hiện giải thích luôn, không cần xác nhận qua nút" | "Muốn hiển thị dạng pop-up, không phải chuyển sang giao diện khác" | **Cả 3 đều gặp friction về UX của Option A**, không phải về mechanism: (1) thiếu visual affordance cho biết từ nào có hỗ trợ, (2) bước xác nhận thừa trước khi thấy giải thích, (3) hình thức hiển thị (modal/bottom-sheet) cảm giác nặng hơn cần thiết |
| Cách lấy lại control | Tester mất thêm một chút thời gian để có thể bôi đen chính xác khái niệm mà chúng tôi muốn giải thích | Bôi đen nhiều chỗ và cuối cùng thì trúng vào chính xác khái niệm | Bôi đen chính xác vào khái niệm cần được giải thích | Cả 3 tester đều mất thêm thời gian để có thể thực sự chọn vào phần khái niệm muốn giải thích |
| Option được chọn | Option A và option B | **"Thích giao diện này (B) nhất, có vẻ khá tiện lợi"** | Option C | Chỉ 1/3 tester nói rõ lựa chọn — **không đủ để tuyên bố "đa số chọn B"**, chỉ là 1 tín hiệu ủng hộ B. Ngoài ra Option B đạt 2/3 vote, Option A và C đều đạt 1/3 vote |
| Trade-off | A: nội dung được đón nhận tích cực ("wow khá là hay haha") nhưng UX có friction | B: "chỉ mất 3s để biết nên tìm ở đâu" — tốc độ là điểm mạnh rõ nhất | C: "ý tưởng ok, nhưng muốn thêm link nguồn dẫn chứng... tóm tắt ngắn quá hơi không tin tưởng" — thiếu evidence làm giảm độ tin cậy | Mỗi option có đúng 1 trade-off nổi bật, không option nào thắng tuyệt đối |

## Concerns bổ sung 

- **Option B:** "Nếu có quá nhiều khái niệm trong một bài học thì mình có mất thời gian tra cứu hơn không?" — lo ngại về khả năng mở rộng (scalability) khi glossary dài ra, danh sách tĩnh có thể mất lợi thế tốc độ hiện tại.
- **Option C:** "Liệu mình có bị làm phiền nếu nó cứ hiện ra như vậy không?" — lo ngại về tần suất trigger, dù ý tưởng chủ động được đón nhận tích cực ("hay đấy, mình thích ý tưởng này").

## Đối chiếu với kỳ vọng ban đầu (Chặng 3 Human–AI Design pass)

- Facilitator annotation của Option A từng giả định *"We expect the tester to: tự tìm ra thao tác bôi đen"* — feedback cho thấy giả định này **không hoàn toàn đúng**: tester tìm ra được nhưng cần thêm affordance trực quan mới tự tin thao tác.
- Human–AI Decision Table của Option C từng ghi *"Evidence/uncertainty: evidence tag 'vì bạn ở lại 15s'"* — feedback cho thấy evidence tag hiện tại **chưa đủ** để tạo lòng tin; tester cần nguồn dẫn chứng cụ thể hơn, không chỉ lý do trigger.

## Một Next Change nhóm chốt

> Giữ **Option B làm cơ chế chính** (do tốc độ tra cứu nhanh nhất và là option duy nhất được nêu rõ là lựa chọn ưa thích), nhưng bổ sung 1 chi tiết vay mượn từ Option A: **gạch chân/visual cue trực tiếp trên thuật ngữ** để neo gợi ý đúng vị trí, thay vì bắt user mở toàn bộ danh sách trong sổ tay. Thay đổi này giải quyết đồng thời 2 pain point từ 2 option khác nhau: "khó biết thuật ngữ nào có hỗ trợ" (từ Option A) và "sợ mất thời gian tra cứu khi nhiều khái niệm" (từ Option B). Option C giữ lại để thử nghiệm tiếp riêng, với 2 sửa đổi trước khi test vòng sau: thêm nguồn dẫn chứng trong bubble giải thích, và cân nhắc lại ngưỡng/tần suất trigger để giảm rủi ro làm phiền.

## Evidence dẫn tới quyết định này

- Tốc độ + được thích nhất: *"mình chỉ mất 3s để biết nên tìm kiếm thông tin ở đâu"*, *"mình thích giao diện này nhất, có vẻ khá tiện lợi"*.
- Thiếu affordance ở A, gây friction dù nội dung được đón nhận tốt: *"cần highlight hoặc có gạch dưới ở khái niệm đó để mình biết khi bấm vào đó thì AI sẽ giải thích"*, *"wow khá là hay haha"*.
- Thiếu độ tin cậy ở C do thiếu nguồn dẫn: *"tóm tắt ngắn gọn quá mình có hơi không tin tưởng"*.

## Still Unproven sau ba feedback

- Việc thêm visual cue (gạch chân) vào Option B có thực sự giải quyết được lo ngại "chậm khi nhiều khái niệm" hay không — mới test với đúng 3 khái niệm (MVE/MVP/PoC), chưa test với glossary dài hơn.
- Ngưỡng làm phiền hợp lý của Option C (bao nhiêu lần trigger là quá nhiều trong 1 buổi học) — mới test 1 lần trigger/tester, chưa test qua nhiều phiên liên tục.
- Việc bỏ bước "xác nhận" ở Option A có thực sự cải thiện trải nghiệm, hay làm mất giá trị cá nhân hoá của bước chẩn đoán — chưa có phép so sánh trực tiếp (A/B test riêng giữa "có chẩn đoán" và "trả lời ngay").
- Thêm link nguồn ở Option C có thực sự tăng độ tin tưởng tương xứng với công sức thêm vào, hay chỉ tạo thêm 1 bước không ai bấm vào — chưa test.

---

## Kết luận:

> Với Hypothesis Problem "learner thiếu kênh xử lý vướng mắc tại chỗ mà không rời luồng học", chúng tôi đã thử ba cách giải (A: AI chẩn đoán qua highlight, B: sổ tay tĩnh, C: AI chủ động theo dwell-time). Tester phản hồi tích cực với ý tưởng của cả 3 nhưng nêu rõ Option B nhanh và tiện nhất trong hiện trạng, đồng thời chỉ ra Option A thiếu affordance trực quan và Option C thiếu độ tin cậy do không có nguồn dẫn chứng — vì vậy iteration tiếp theo chúng tôi sẽ giữ cơ chế tra cứu tĩnh của B làm nền, bổ sung visual cue kiểu Option A ngay trên thuật ngữ, và tiếp tục thử nghiệm riêng Option C sau khi thêm nguồn dẫn chứng và điều chỉnh ngưỡng trigger.
