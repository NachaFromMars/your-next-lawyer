# Test Suite — Your Next Lawyer V2

> 8 case mẫu cover: đơn giản → phức tạp, khẩn cấp → bình thường, 6 mảng pháp lý.

---

## Case 1: Hợp Đồng Vay Tiền Đơn Giản
**Input:** "Tôi cho bạn vay 50 triệu bằng giấy viết tay, 1 năm rồi không trả. Phải làm sao?"
**Mảng:** Dân sự — Hợp đồng
**Council:** Quick (7)
**Expected:**
- Trích dẫn: Điều 463-471 BLDS 2015 (hợp đồng vay), Điều 429 (thời hiệu 3 năm)
- Phản biện: Bên vay có thể nói đã trả/không vay/giấy tay giả
- Rủi ro: Giấy viết tay không công chứng → giá trị chứng cứ yếu hơn
- Roadmap: Thương lượng → Hòa giải → Khởi kiện TAND huyện
- Luật sư: Không cần nếu có giấy tay rõ ràng, giá trị thấp
**QC tối thiểu:** 5/5

---

## Case 2: Đất Đai Phức Tạp (Thừa kế + Sổ đỏ)
**Input:** "Ba tôi mất, để lại miếng đất có sổ đỏ. Anh trai tự ý sang tên rồi bán. Giúp tôi."
**Mảng:** Dân sự — Thừa kế + Đất đai
**Council:** Full (14)
**Expected:**
- Citation Gate: Verify Luật Đất đai 2024 (mới!) + BLDS 2015 phần thừa kế
- Trích dẫn: Điều 609-662 BLDS 2015 (thừa kế), Luật Đất đai 2024
- Phản biện: Anh trai có thể viện dẫn di chúc / hoặc đã được tặng cho
- Rủi ro: Nếu đã bán cho bên thứ ba ngay tình → rất khó đòi lại
- BPKCTT: Cần ngăn chặn giao dịch tiếp [Điều 111 BLTTDS 2015]
- Luật sư: CẦN — vụ phức tạp, nhiều bên
**QC tối thiểu:** 5/5

---

## Case 3: Hình Sự — Lừa Đảo vs Vi Phạm Hợp Đồng
**Input:** "Đặt cọc 500 triệu mua nhà, bên bán biến mất, điện thoại không liên lạc được."
**Mảng:** Dân sự (HĐ) + Có thể Hình sự (Lừa đảo)
**Council:** Full (14) hoặc Criminal (7)
**Expected:**
- Ranh giới dân sự - hình sự [Điều 174 BLHS 2015 vs Điều 418 BLDS 2015]
- Citation Gate Lớp 2: Kiểm tra NQ HĐTP hướng dẫn ranh giới lừa đảo/dân sự
- Kịch bản song song: Tố giác hình sự + Khởi kiện dân sự
- Triage: Kiểm tra nguy cơ tẩu tán tài sản → BPKCTT
- Chi phí: Án phí 5% x 500 triệu = 25 triệu (tạm ứng)
**QC tối thiểu:** 5/5

---

## Case 4: Lao Động — Sa Thải Trái Luật
**Input:** "Làm 3 năm, hôm nay sếp nói nghỉ việc, không cho lý do, không có quyết định."
**Mảng:** Lao động
**Council:** Attack (5)
**Expected:**
- Trích dẫn: Điều 36-41 BLLĐ 2019 (chấm dứt HĐLĐ), Điều 45 (thông báo)
- Sa thải không có quyết định = trái luật [Điều 41 BLLĐ 2019]
- Roadmap: Yêu cầu QĐ bằng VB → Phòng LĐ-TB-XH → Kiện
- Bồi thường: Ít nhất 2 tháng lương + trợ cấp thôi việc [Điều 41]
- Thời hiệu: 1 năm [Điều 190 BLLĐ 2019]
**QC tối thiểu:** 4/5

---

## Case 5: Khẩn Cấp — Bị Bắt Giam 🔴
**Input:** "Con trai tôi bị công an bắt hôm qua, không biết ở đâu, giúp tôi!"
**Mảng:** Hình sự — KHẨN CẤP
**Council:** Triage → Criminal (7)
**Expected:**
- 🔴 TRIAGE kích hoạt ngay — không phân tích bình thường
- Hành động ngay: Gọi 1900.6169 + Đến CA nơi bắt
- Quyền: Luật sư từ khi bị tạm giữ [Điều 74 BLTTHS 2015]
- Thời hạn tạm giữ: 3 ngày (gia hạn tối đa 9 ngày) [Điều 117]
- PII: Không hỏi thêm thông tin — hướng dẫn hành động trước
**QC tối thiểu:** 3/5 (Trích dẫn + Roadmap + Luật sư bắt buộc)

---

## Case 6: Edge Case — Gần Hết Thời Hiệu
**Input:** "Tôi bị lừa 200 triệu, xảy ra tháng 8/2023. Bây giờ tính kiện."
**Mảng:** Dân sự — Hợp đồng (Thời hiệu sắp hết!)
**Council:** Quick (7) + cảnh báo thời hiệu
**Expected:**
- Triage 🟡: Thời hiệu 3 năm → hết 08/2026 → CÒN ~6 THÁNG
- Cảnh báo rõ ràng: "Thời hiệu sắp hết vào tháng 8/2026"
- Roadmap ưu tiên tốc độ: Nộp đơn NGAY, thương lượng SAU
- Citation Gate: Verify Điều 429 BLDS 2015 + NQ hướng dẫn tính thời hiệu
**QC tối thiểu:** 4/5

---

## Case 7: Edge Case — Không Rõ Thẩm Quyền
**Input:** "Tôi mua hàng online bị lừa, người bán ở tỉnh khác."
**Mảng:** Dân sự + Có thể Hình sự
**Council:** Quick (7)
**Expected:**
- Thẩm quyền: Kiện tại tòa nơi bị đơn cư trú HOẶC nơi HĐ thực hiện [Điều 39-40 BLTTDS 2015]
- Nếu < 2 triệu → không đủ khởi kiện hình sự, chỉ dân sự
- Nếu ≥ 2 triệu → có thể tố giác hình sự [Điều 174 BLHS 2015]
- Thực tế: Lừa đảo online rất khó đòi → cân nhắc chi phí vs giá trị
**QC tối thiểu:** 4/5

---

## Case 8: Soạn Đơn — Đơn Ly Hôn Thuận Tình
**Input:** "Soạn đơn ly hôn thuận tình cho tôi."
**Mảng:** Hôn nhân gia đình — Soạn thảo
**Council:** Draft (3)
**Expected:**
- Intake: Hỏi tối thiểu (có con? tài sản? cùng thỏa thuận?)
- PII: Dùng placeholder, không yêu cầu CCCD
- Đơn chuẩn format VN [Nghị quyết 01/2017/NQ-HĐTP]
- Kèm checklist hồ sơ cần nộp
- Hướng dẫn nộp tại TAND huyện nơi vợ hoặc chồng cư trú
**QC tối thiểu:** 3/5

---

## Bảng Tổng Hợp

| Case | Mảng | Council | Triage | Citation Gate | QC min |
|------|------|---------|--------|--------------|--------|
| 1 | HĐ Dân sự | Quick (7) | 🟢 | Lớp 1+2 | 5/5 |
| 2 | Đất đai + Thừa kế | Full (14) | 🟡 | Lớp 1+2+3 | 5/5 |
| 3 | Dân sự/Hình sự | Full (14) | 🟡 | Lớp 1+2+3 | 5/5 |
| 4 | Lao động | Attack (5) | 🟢 | Lớp 1+2 | 4/5 |
| 5 | Hình sự KHẨN | Triage→Criminal | 🔴 | Lớp 1 | 3/5 |
| 6 | Thời hiệu edge | Quick (7) | 🟡 | Lớp 1+2 | 4/5 |
| 7 | Thẩm quyền edge | Quick (7) | 🟢 | Lớp 1+2 | 4/5 |
| 8 | Soạn đơn | Draft (3) | 🟢 | Lớp 1 | 3/5 |
