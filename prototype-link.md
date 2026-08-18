# Prototype Links — Case A: AI Tutor

Ba micro-prototype HTML click-through, dùng chung 1 content fixture (slide "MVE, MVP, PoC"). Mỗi bản là 1 file độc lập, mở trực tiếp bằng trình duyệt — không cần server hay cài đặt gì thêm.

| Bản | Option | File | Mở bằng |
|---|---|---|---|
| Bản 1 | A — Highlight-to-ask + AI chẩn đoán | [`prototype/a.html`](prototype/option_a.html) | Double-click hoặc kéo vào tab trình duyệt |
| Bản 2 | B — Sổ tay tĩnh, không AI | [`prototype/b.html`](prototype/option_b.html) | Double-click hoặc kéo vào tab trình duyệt |
| Bản 3 | C — AI chủ động phát hiện (dwell-time 15s) | [`prototype/c.html`](prototype/option_c.html) | Double-click hoặc kéo vào tab trình duyệt |

## Cách dùng khi test (facilitator)

- Mỗi file có nút **↺ Reset** (góc trên) để đưa prototype về common context giữa các tester.
- Mỗi file có nút **👁 Facilitator notes** — hiện mechanism, "We expect / Watch for / Do not explain" cho riêng option đó. **Không cho tester thấy panel này.**
- Task banner (🎯) trong mỗi file đã đồng bộ, đúng outcome task ở Chặng 5 — không cần facilitator giải thích thêm.
- Bản 3 (Option C) cần tester ở lại slide **≥15 giây không tương tác** để thấy được bubble AI — nếu chuyển bản quá nhanh sẽ bỏ lỡ interaction chính.

