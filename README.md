# Track 1 - Day 18 — Multiple Prototypes: Human–AI Design

## 1. Thông tin cá nhân và nhóm

- **MHV:** 2A202601645
- **Họ và tên:** Lê Minh Khiêm
- **Tên nhóm:** Bàn 1
- **Ba thành viên:**
  1. Lê Hà Hải Vân — 2A202601587
  2. Lê Minh Khiêm — 2A202601645
  3. La Thị Thanh Tuyết — 2A202601589
- **Case đã chọn:** Case A — AI Tutor: Diagnostic Refresher (tiếp tục từ Day 17)

---

## 2. Hypothesis Problem (dùng trong Day 18)

> Khi đang học và gặp một phần nội dung chưa hiểu (vì thiếu nghĩa thuật ngữ, thiếu giải thích tại chỗ, hoặc giảng viên đi nhanh), learner khó tiếp tục theo kịp bài giảng vì không có cách xử lý vướng mắc ngay tại chỗ mà không phải rời luồng học để tự tra cứu (chatbot nội bộ, Google, AI ngoài) — dẫn đến bỏ lỡ nội dung tiếp theo, dồn nợ kiến thức và mất mạch bài giảng.

**Evidence Day 17 hỗ trợ:** 3/3 Practice Notes (Vân — PV001, Tuyết — PV002, Khiêm — Tuấn 01149) đều có cùng pattern: rời luồng bài học để tự tra cứu (chatbot nội bộ và/hoặc AI ngoài/Google), và cùng hậu quả mất mạch/bỏ lỡ nội dung tiếp theo — dù root cause "chưa hiểu" khác nhau ở mỗi người.

**Điều vẫn chưa được chứng minh:** root cause nào (từ vựng / slide thiếu giải thích / tốc độ giảng) phổ biến nhất; rào cản "ngại hỏi vì sợ câu hỏi quá cơ bản" (chỉ xuất hiện ở note Khiêm) có lặp lại ở người khác không.

*Chi tiết đầy đủ chuỗi Solution → Evidence: xem [`three-option-design-sheet.md`](three-option-design-sheet.md).*

---

## 3. Three Solution Options

| Bản | Option | Mô tả ngắn | Link |
|---|---|---|---|
| Bản 1 | **A — Highlight-to-ask** | Bôi đen thuật ngữ → AI hỏi 1 câu chẩn đoán → chọn mức giải thích phù hợp → có thể chat hỏi thêm | [`prototype/a.html`](prototype/a.html) |
| Bản 2 | **B — Sổ tay tĩnh** | Bấm nút mở sổ tay chứa định nghĩa viết sẵn, không có AI suy luận | [`prototype/b.html`](prototype/b.html) |
| Bản 3 | **C — AI chủ động phát hiện** | Ở lại slide ≥15 giây không tương tác → AI chủ động đề xuất giải thích | [`prototype/c.html`](prototype/c.html) |

Chi tiết Human–AI Decision Table và Comparison Contract: xem [`three-option-design-sheet.md`](three-option-design-sheet.md). Link tổng hợp cách mở/test cả 3: xem [`prototype-link.md`](prototype-link.md).

---

## 4. Đóng góp của tôi trong nhóm

> Tôi đã tham gia tổng hợp evidence, xây dựng Design Sheet + Human–AI Decision Table, build và sửa cả 3 micro-prototype qua nhiều vòng review (phát hiện và sửa lỗi lộ mechanism, khôi phục đúng mục đích Option A, đổi trigger Option C). Sau Chặng 6, tôi tổng hợp feedback thô của cả nhóm thành Group Feedback Synthesis.

---

## 5. Prototype Feedback

- Observation từ phiên tôi facilitate: xem [`prototype-feedback-note.md`](prototype-feedback-note.md)
- Ba-feedback synthesis, Next Change, Still Unproven: xem [`group-feedback-synthesis.md`](group-feedback-synthesis.md)

---

## 6. AI Support Log

Xem đầy đủ tại [`ai-support-log.md`](ai-support-log.md). Tóm tắt: AI hỗ trợ dựng Design Sheet, Human–AI Decision Table, code prototype và rà soát lỗi thiết kế (lộ mechanism, task banner không đồng nhất). Lỗi tôi đã tự sửa: Option A từng bị lược mất bước chẩn đoán khi tôi tự chỉnh UI.

---

## Cấu trúc repo

```
Track1_Day18_2A202601587_LeHaHaiVan/
├── README.md
├── three-option-design-sheet.md
├── prototype-link.md
├── prototype-feedback-note.md     
├── group-feedback-synthesis.md    
├── ai-support-log.md
└── prototype/
    ├── option_a.html
    ├── option_b.html
    └── option_c.html
```
