# AI Support Log — Lê Hà Hải Vân

**AI đã giúp tôi ở đâu?**

- Chặng 2–3: dựng Human–AI Decision Table (expectation, role/agency, evidence/uncertainty, control/recovery) cho từng option.
- Chặng 4: viết code HTML cho micro-prototype ban đầu của option A; sau đó tiếp tục sửa theo yêu cầu cụ thể của tôi qua nhiều vòng (giữ đúng bước chẩn đoán cho Option A, ẩn mechanism khỏi tester, đồng bộ task banner, thêm nút reset).
- Chặng 5: soạn Test Prompt, Observation Focus và nhắc lại luật facilitation.
- Rà soát: tự phát hiện 2 lỗi nghiêm trọng trong bản UI tôi tự chỉnh (header lộ mechanism cho tester, task banner khác nhau giữa 3 file) trước khi tôi kịp mang đi test thật.

**AI sai, hời hợt hoặc làm các options giống nhau ở đâu?**

- Ở lần build đầu, AI vô tình để lộ mô tả mechanism ngay trên header mỗi trang.

**Tôi đã tự sửa hoặc quyết định lại điều gì?**

- Yêu cầu AI khôi phục đúng mục đích ban đầu của Option A (AI phải chẩn đoán trước khi giải thích, đúng với solution directive gốc), thay vì giữ bản đã lược bớt.
- Yêu cầu ẩn toàn bộ mechanism khỏi tester và đồng bộ task banner.
