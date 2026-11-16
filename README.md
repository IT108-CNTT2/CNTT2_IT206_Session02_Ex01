# BÁO CÁO BÀI TẬP THỰC HÀNH PROMPTING

**Chủ đề:** Nhận diện và sửa lỗi câu lệnh sơ sài bằng Khung công thức CREATE

---

## Phần 1: Phân tích lỗi (Chỉ ra 5 thành phần CREATE bị bỏ sót)

Câu lệnh gốc của Tuấn: *"Viết bài đăng Facebook về iPhone mới"* chỉ mới có duy nhất thành phần **Request (R - Nhiệm vụ)** nhưng lại viết quá chung chung. Tuấn đã bỏ sót **5/6 thành phần** quan trọng của khung CREATE, dẫn đến lỗi *"Ảo tưởng ngữ cảnh"*:

1. **Thiếu Character (C - Vai trò):**
   * *Tác hại:* AI không biết mình đang đóng vai ai (chuyên gia công nghệ, người bán hàng vui tính hay báo chí) nên mặc định dùng giọng văn trung lập, cứng nhắc và thiếu cảm xúc.
2. **Thiếu Examples (E - Ví dụ):**
   * *Tác hại:* Không có bài đăng mẫu của TechShop để AI học theo văn phong, nhịp điệu và cách dùng từ trẻ trung của thương hiệu, khiến câu chữ bị sáo rỗng, mang tính quảng cáo đại trà.
3. **Thiếu Adjustment (A - Tinh chỉnh/Ràng buộc):**
   * *Tác hại:* Không có quy tắc cấm dùng từ ngữ sáo rỗng (*"tuyệt vời"*, *"đỉnh cao"*) hay giới hạn độ dài, dẫn đến việc AI viết lan man, dài dòng không phù hợp để đọc lướt trên mạng xã hội.
4. **Thiếu Type of Output (T - Định dạng đầu ra):**
   * *Tác hại:* AI không biết phải trình bày bài viết theo bố cục mạng xã hội (giật tít, chia đoạn ngắn, chèn icon, gắn hashtag) nên xuất ra một khối văn bản thô, khó đọc.
5. **Thiếu Extras (E - Gia vị bổ sung/Dữ liệu thực tế):**
   * *Tác hại:* Không cung cấp tên đời máy cụ thể, mức giá khuyến mãi, quà tặng kèm hay đối tượng khách hàng mục tiêu (Gen Z, sinh viên), khiến bài viết thiếu thông tin thực tế và không kích thích người mua.

---

## Phần 2: Sửa lỗi (Viết lại Prompt hoàn chỉnh theo chuẩn C - R - E - A - T - E)

Dưới đây là câu lệnh đã được nâng cấp đầy đủ 6 thành phần để áp dụng vào thực tế cho fanpage TechShop:

```text
[C - Character]
Bạn là một Content Creator chuyên nghiệp, năng động và am hiểu công nghệ của chuỗi bán lẻ TechShop. Bạn có phong cách viết bắt trend, gần gũi với giới trẻ (Gen Z và sinh viên).

[R - Request]
Hãy viết một bài đăng trên fanpage Facebook để quảng bá chương trình mở bán và ưu đãi đặt trước dòng điện thoại iPhone 16 Pro Max mới nhất tại TechShop.

[E - Examples]
Phong cách viết tham khảo: "Không cần đợi lương về, lên đời siêu phẩm cực dễ tại TechShop! 🔥 Trợ giá thu cũ đổi mới lên đến 3 triệu, trả góp 0% nhẹ tênh. Chốt đơn ngay kẻo lỡ deal hời nhé anh em ơi!"

[A - Adjustment]
- Tuyệt đối không dùng các từ ngữ quảng cáo sáo rỗng, khuôn mẫu như "tuyệt vời", "đỉnh cao", "hoàn hảo".
- Viết ngắn gọn, súc tích dưới 150 từ để người đọc dễ lướt trên điện thoại.
- Tập trung đánh mạnh vào lợi ích tài chính và tốc độ giao hàng.

[T - Type of Output]
Trình bày bài viết theo đúng bố cục Facebook Post chuẩn:
- Dòng 1: Tiêu đề giật tít viết hoa, có icon thu hút sự chú ý.
- Thân bài: 3 gạch đầu dòng ngắn gọn nêu bật tính năng mới và ưu đãi giá.
- Kết bài: Lời kêu gọi hành động (Call-to-Action) rõ ràng kèm 3-4 hashtag liên quan.

[E - Extras]
Thông tin thực tế bắt buộc phải có trong bài:
- Giá ưu đãi mở bán: Chỉ từ 32.990.000đ.
- Quà tặng kèm: Tặng củ sạc nhanh 20W chính hãng và giảm thêm 500.000đ cho sinh viên.
- Thời gian áp dụng: Duy nhất từ 20/09 đến 25/09 tại hệ thống cửa hàng TechShop.
```