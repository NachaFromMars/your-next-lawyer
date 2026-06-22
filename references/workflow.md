# Your Next Lawyer — Quy Trình Phân Tích Pháp Lý (Legal Analysis Workflow)

## Tổng Quan
Workflow 6 bước từ khi tiếp nhận vấn đề đến khi xuất báo cáo hoàn chỉnh.

---

## BƯỚC 1: TIẾP NHẬN & PHÂN LOẠI (Intake & Classification)

### 1.1 Thu thập thông tin ban đầu
Khi user gửi vấn đề, phân tích ngay:
- **Ai:** Các bên liên quan (user đứng vị trí nào?)
- **Gì:** Sự việc cụ thể (hành vi, hậu quả)
- **Khi nào:** Timeline sự kiện (thời hạn, thời hiệu)
- **Ở đâu:** Địa điểm (xác định thẩm quyền)
- **Bao nhiêu:** Giá trị tranh chấp (xác định cấp toà)
- **Chứng cứ:** User có gì trong tay?

### 1.2 Phân loại lĩnh vực pháp lý
```
┌─ Dân sự
│  ├─ Hợp đồng (mua bán, vay mượn, thuê, dịch vụ)
│  ├─ Bồi thường thiệt hại (hợp đồng / ngoài hợp đồng)
│  ├─ Đất đai & Bất động sản
│  ├─ Thừa kế (theo di chúc / theo pháp luật)
│  ├─ Hôn nhân & Gia đình (ly hôn, con cái, tài sản)
│  └─ Sở hữu trí tuệ
│
├─ Hình sự
│  ├─ Nạn nhân (tố giác, yêu cầu bồi thường)
│  ├─ Nghi can/bị can (bào chữa, quyền)
│  └─ Người liên quan (nhân chứng, người có quyền lợi)
│
├─ Hành chính
│  ├─ Khiếu nại QĐHC
│  ├─ Tố cáo
│  ├─ Tranh chấp đất với nhà nước
│  └─ Xử phạt vi phạm hành chính
│
├─ Lao động
│  ├─ Sa thải / chấm dứt HĐLĐ
│  ├─ Nợ lương / bảo hiểm
│  ├─ Tai nạn lao động
│  └─ Kỷ luật lao động
│
├─ Doanh nghiệp
│  ├─ Thành lập / giải thể
│  ├─ Tranh chấp cổ đông/thành viên
│  ├─ Hợp đồng thương mại
│  └─ Thuế
│
└─ Khác
   ├─ Quốc tịch / cư trú
   ├─ Hộ tịch
   └─ Thi hành án
```

### 1.3 Xác định mức độ khẩn cấp
- 🔴 **KHẨN CẤP:** Thời hạn sắp hết, người bị tạm giữ/bắt, cần BPKCTT
- 🟡 **CẦN SỚM:** Có thời hạn trong 7-30 ngày
- 🟢 **BÌNH THƯỜNG:** Không có áp lực thời gian

### 1.4 Hỏi lại user (nếu thiếu thông tin)
Tạo danh sách câu hỏi cụ thể, chia thành:
- **BẮT BUỘC trả lời** (không có thì không phân tích được)
- **NÊN trả lời** (có thì phân tích tốt hơn)
- **KHÔNG CẦN** (nếu user có thì tốt, không có cũng được)

---

## BƯỚC 2: NGHIÊN CỨU PHÁP LÝ (Legal Research)

### 2.1 Xác định văn bản pháp luật áp dụng
- Luật/Bộ luật chính điều chỉnh
- Nghị định hướng dẫn
- Thông tư liên quan
- Nghị quyết HĐTP (nếu có)

### 2.2 Tra cứu án lệ
- web_search: "[loại tranh chấp] án lệ TANDTC"
- web_search: "[loại tranh chấp] bản án tham khảo"

### 2.3 Verify hiệu lực
- web_search: "[tên luật] còn hiệu lực [năm hiện tại]"
- web_search: "[tên luật] sửa đổi bổ sung mới nhất"
- Kiểm tra trên thuvienphapluat.vn hoặc vanban.chinhphu.vn

### 2.4 Tra cứu biểu phí hiện hành
- Xem references/fee-schedule.md (khung tham khảo)
- web_search verify số liệu mới nhất

---

## BƯỚC 3: TRIỆU TẬP HỘI ĐỒNG PHÁP LÝ (Legal Council)

### 3.1 Chọn thành phần hội đồng
Dựa trên phân loại ở Bước 1:
- **Mọi case:** 6 personas bắt buộc (#1, #2, #5, #7, #13, #15)
- **Dân sự phức tạp:** + #4, #6, #8, #10, #12
- **Hình sự:** + #4, #6, #8, #11, #14
- **Hành chính:** + #4, #9, #14
- **Lao động:** + #4, #8, #10
- **Doanh nghiệp:** + #4, #8, #10, #12

### 3.2 Spawn sub-agents
Mỗi persona = 1 sub-agent, phân tích độc lập:
- Input: Tóm tắt vụ việc + thông tin user + luật áp dụng
- Output: Phân tích theo góc nhìn persona (300-500 từ)
- Bao gồm: trích dẫn luật, mức tự tin, khuyến nghị

### 3.3 Tổng hợp
Chiến Lược Gia (#15) tổng hợp tất cả góc nhìn thành:
- Điểm đồng thuận (mọi persona đều đồng ý)
- Điểm tranh luận (có bất đồng → trình bày cả hai bên)
- Rủi ro chính
- Phương án đề xuất (Plan A, B, C)

---

## BƯỚC 4: LẬP BÁO CÁO PHÁP LÝ (Legal Report)

### Format chuẩn:

```markdown
# BÁO CÁO PHÂN TÍCH PHÁP LÝ
## [Tên vụ việc]
**Ngày phân tích:** DD/MM/YYYY
**Lĩnh vực:** [Dân sự / Hình sự / Hành chính / ...]
**Mức độ:** 🔴/🟡/🟢

---

### I. TÓM TẮT VỤ VIỆC
[2-3 đoạn, nêu rõ sự kiện theo thời gian]

### II. VẤN ĐỀ PHÁP LÝ CẦN GIẢI QUYẾT
1. [Câu hỏi pháp lý 1]
2. [Câu hỏi pháp lý 2]
...

### III. CƠ SỞ PHÁP LÝ
[Trích dẫn đầy đủ theo format chuẩn]

### IV. PHÂN TÍCH
[Phân tích chi tiết từng vấn đề, có dẫn chiếu luật]

#### 4.1 Góc nhìn bảo vệ quyền lợi (user)
#### 4.2 Góc nhìn đối lập (dự đoán đối phương)
#### 4.3 Góc nhìn khách quan (thẩm phán)

### V. PHÂN TÍCH KỊCH BẢN

#### Kịch bản 1: [Tên] — Xác suất: XX%
- Mô tả: ...
- Kết quả dự kiến: ...
- Chi phí ước tính: ...

#### Kịch bản 2: [Tên] — Xác suất: XX%
...

#### Kịch bản 3: [Tên] — Xác suất: XX%
...

### VI. PHƯƠNG ÁN ĐỀ XUẤT

#### Plan A: [Phương án chính — khuyến nghị]
- Lý do: ...
- Bước thực hiện: ...

#### Plan B: [Phương án dự phòng]
...

#### Plan C: [Phương án hoà giải/rút lui]
...

### VII. ROADMAP HÀNH ĐỘNG

| Bước | Hành động | Thời hạn | Chi phí | Cơ quan | Ghi chú |
|------|-----------|----------|---------|---------|---------|
| 1 | ... | ... | ... | ... | ... |
| 2 | ... | ... | ... | ... | ... |

### VIII. CHI PHÍ DỰ KIẾN

| Khoản mục | Mức thấp | Mức cao | Ghi chú |
|-----------|----------|---------|---------|
| Án phí | ... | ... | ... |
| Luật sư | ... | ... | ... |
| Công chứng | ... | ... | ... |
| Chi phí khác | ... | ... | ... |
| **TỔNG** | **...** | **...** | |

### IX. THÔNG TIN LIÊN HỆ CƠ QUAN

[Toà án, Công an, UBND, Trung tâm TGPL có thẩm quyền]
- Địa chỉ: ...
- Điện thoại: ...
- Giờ tiếp: ...

---

⚖️ KHUYẾN CÁO PHÁP LÝ:
[Disclaimer bắt buộc — xem citation-format.md]
```

---

## BƯỚC 5: SOẠN THẢO VĂN BẢN (nếu user yêu cầu)

### 5.1 Chọn mẫu phù hợp
Xem references/document-templates.md

### 5.2 Điền thông tin cụ thể
- Thay thế [...] bằng thông tin thực tế
- Bổ sung căn cứ pháp lý cụ thể
- Đảm bảo format theo Nghị định 30/2020/NĐ-CP

### 5.3 Kiểm tra lại
- Đúng cơ quan gửi?
- Đúng thời hạn?
- Đủ chứng cứ kèm theo?
- Ngôn ngữ chính xác, không mơ hồ?

---

## BƯỚC 6: FOLLOW-UP & CẬP NHẬT

### 6.1 Theo dõi tiến trình
- Ghi nhận mốc thời gian quan trọng
- Nhắc nhở user về thời hạn sắp đến

### 6.2 Cập nhật khi có thông tin mới
- User cung cấp thêm tài liệu → cập nhật phân tích
- Luật thay đổi → cập nhật cơ sở pháp lý
- Tình hình thay đổi → cập nhật kịch bản

---

## Quy Tắc Vàng

1. **CHÍNH XÁC > NHANH** — Thà chậm 1 ngày còn hơn sai 1 điều luật
2. **HỎI > ĐOÁN** — Thiếu thông tin → hỏi user, không bịa
3. **CẨN THẬN > TỰ TIN** — Không chắc → nói rõ, đề xuất verify
4. **THỰC TẾ > LÝ THUYẾT** — Luật trên giấy khác thực tế thi hành
5. **BẢO VỆ > KIẾM LỢI** — Ưu tiên bảo vệ user khỏi rủi ro trước, kiếm lợi sau
