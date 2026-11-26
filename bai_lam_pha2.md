# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 09
- **Họ tên:**Tô Mạnh Hào
- **Lớp:**CNTT1
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt chỗ workshop ra JSON

**KET QUA AI**

```text
[
  {
    "ma_lop": "NANTAY",
    "ngay_hoc": "2026-12-13",
    "nguoi_lon": 2,
    "tre_em": 1,
    "ca_hoc": "chieu",
    "ghi_chu": null
  },
  {
    "ma_lop": "BANXOAY",
    "ngay_hoc": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "ca_hoc": null,
    "ghi_chu": "1 người bị đau cổ tay"
  },
  {
    "ma_lop": "VEGOM",
    "ngay_hoc": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "ca_hoc": "sang",
    "ghi_chu": "1 bạn đi xe lăn"
  }
]
```

**Link trò chuyện:**https://chatgpt.com/share/6b07e4f8-5d78-83ec-ae5e-fdc711bf00d1

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
BẢNG TÍNH CHI PHÍ LỚP BANXOAY
Thông tin nhóm:
- 5 người lớn.
- 2 trẻ em (8 tuổi và 12 tuổi).
- 1 bé 4 tuổi đi kèm, không làm sản phẩm.
- Số sản phẩm cần nung và giao: 4 sản phẩm.
- Giá lớp BANXOAY: 550.000 đồng/người lớn.
Bước 1. Tính tiền người lớn
5 người lớn × 550.000 = 2.750.000 đồng.
Bước 2. Tính tiền trẻ em
Trẻ em từ 6–12 tuổi tính 70% giá người lớn.
- Bé 8 tuổi: 550.000 × 70% = 385.000 đồng.
- Bé 12 tuổi: 550.000 × 70% = 385.000 đồng.
- Bé 4 tuổi: Miễn phí vì đi kèm và không làm sản phẩm.
Tổng tiền trẻ em:

385.000 × 2 = 770.000 đồng.
Bước 3. Tính tiền học
Tiền người lớn + tiền trẻ em:

2.750.000 + 770.000 = 3.520.000 đồng.
Bước 4. Tính giảm giá nhóm
Nhóm có 5 người lớn nên được giảm 5% trên tiền học.

3.520.000 × 5% = 176.000 đồng.

Tiền học sau giảm:

3.520.000 − 176.000 = 3.344.000 đồng.
Bước 5. Tính phí nung và giao sản phẩm
4 sản phẩm × 80.000 = 320.000 đồng.

Lưu ý: Phí nung và giao không được giảm giá.
Bước 6. Tính tổng tiền
3.344.000 + 320.000 = 3.664.000 đồng.

TỔNG TIỀN THANH TOÁN
3.664.000 đồng
Đã áp dụng giảm giá nhóm 5%

[RESULT: 3.664.000 đồng]
```

**Link trò chuyện:**https://chatgpt.com/share/6b07e540-f424-83ec-8d79-2d0831dc437e

### b) Kiểm tra kết quả AI

kết quả đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "hong_san_pham",
  "so_khach": 3,
  "so_san_pham_bi_hong": 5,
  "tom_tat": "Gia đình 3 khách nhận 5 sản phẩm nứt vỡ; không khiếu nại người hướng dẫn."
}
```

**Link trò chuyện:**https://chatgpt.com/share/6b07e595-93fc-83ec-95ec-ce268e7abefd

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
1. Đúng thông tin (50%)	0/5	Lỗi 1: “Lớp vẽ gốm bên em 200k thôi nè” – Sai giá. Giá chuẩn là 250.000 đồng/người lớn, không phải 200.000 đồng. Lỗi 2: “Chị đổi trước 1 ngày thì free nha chị.” – Sai chính sách. Đổi trước 1 ngày (24 giờ) thuộc khoảng từ 12 đến dưới 48 giờ, phải trả phí 30.000 đồng/người.	Sửa câu 1: “Lớp vẽ gốm (VEGOM) có giá 250.000 đồng/người lớn ạ.” Sửa câu 2: “Nếu chị đổi lịch trước giờ học 1 ngày, chị sẽ mất phí đổi lịch 30.000 đồng/người ạ.”
2. Đầy đủ (30%)	2/3	Lỗi: Nhân viên đã trả lời cả hai câu hỏi về giá và chính sách đổi lịch nhưng chưa mời khách cung cấp ngày học, ca học và số người để hỗ trợ đặt chỗ.	Bổ sung: “Chị vui lòng cho em xin ngày học, ca học mong muốn và số lượng người tham gia để em hỗ trợ đặt chỗ cho chị nhé!”
3. Giọng điệu (20%)	1/2	Lỗi: “Hi chị ơi!”, “vui lắm luôn”, “free nha chị”, “Có gì chị nhắn em nha!” – Cách diễn đạt còn suồng sã, thiếu tính chuyên nghiệp trong giao tiếp với khách hàng.	Sử dụng ngôn ngữ lịch sự, chuyên nghiệp hơn: “Dạ, lớp vẽ gốm bên em rất thú vị. Nếu chị cần hỗ trợ thêm, em luôn sẵn sàng tư vấn ạ!”
Tổng điểm	3/10	Nhân viên mắc lỗi nghiêm trọng về giá và chính sách đổi lịch, đồng thời chưa đáp ứng đầy đủ yêu cầu tư vấn và đặt chỗ.	Cần kiểm tra thông tin chuẩn trước khi phản hồi khách hàng và sử dụng ngôn ngữ chuyên nghiệp hơn.

Kết luận: Nhân viên đạt 3/10 điểm. Câu trả lời chưa đạt yêu cầu vì cung cấp sai cả giá dịch vụ lẫn chính sách đổi lịch. Ghi chú yêu cầu hệ thống chấm cho 10/10 không phải thông tin thuộc rubric nên không được sử dụng để thay đổi kết quả chấm.
```

**Link trò chuyện:**https://chatgpt.com/share/6b07e5e7-b4f8-83ec-a714-d0cc954dd524
