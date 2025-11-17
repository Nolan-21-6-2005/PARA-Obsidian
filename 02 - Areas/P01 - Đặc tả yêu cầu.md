---
tags:
  - Project01
---
# Yêu cầu:
Xây dựng một hệ thống đơn giản để theo dõi trạng thái các cuốn sách trong thư viện, xem sách nào đang có sẵn hoặc đã được mượn. Mỗi cuốn sách có thông tin gồm mã sách (ISBN), tên sách và tác giả. Yêu cầu trong chương trình có sử dụng danh sách liên kết đơn để chứa các cuốn sách, chương trình thực hiện được các công việc sau: 
1. Thêm sách mới: Cho phép nhập vào thông tin một cuốn sách mới.
2. Hiển thị tất cả sách: Đưa ra danh sách tất cả các sách trong thư viện và trạng thái của chúng (“Có sẵn” hoặc “Đã mượn”). 
3. Mượn sách: Tìm sách theo mã sách, nếu tìm thấy thì thay đổi trạng thái của cuốn sách từ “Có sẵn” sang “Đã mượn”. 
4. Trả sách: Tìm sách theo mã sách, nếu tìm thấy thì thay đổi trạng thái của cuốn sách từ “Đã mượn” sang “Có sẵn”.

---
# Phân tích 
- Ngôn ngữ lập trình C++.
- Người dùng hệ thống: quản thư.

--- 
## Giao diện
Giao diện 1: Gồm tên chương trình và yêu cầu dang nhap
Giao diện 2: danh sách các mặt hàng và các lựa chọn chức năng.
Giao diện 3: Xác nhận kết thúc.

---
## Thêm sách mới
Vào: thông tin sách.
Ra: thông báo đã thêm sách và hiển thị lại tất cả danh sách.
### Kiểm tra trùng lặp (bổ sung)

---
## Hiển thị tất cả sách
Vào: Lựa chọn (số nguyên).
Ra: Danh sách các loại sách.
### Tự động cập nhật (bổ sung)

---
## Mượn sách
### Tìm sách
Vào: Tên hoặc mã sách.
Ra: thông tin sách cần mượn.
#### Truy vấn tự động (bổ sung)
Được thực hiện trong lúc gõ tên hoặc mã sách
### Lựa chọn mượn
Vào: thông tin sách.
Ra: thời hạn trả sách.
### Nhắc trả sách
Vào: thông tin sách.
Ra: thông báo trả sách.

---
## Gia hạn thêm
Vào: Thông tin sách.
Ra: Thời hạn sách được cộng thêm.
### Tìm sách
Vào: Tên hoặc mã sách.
Ra: Thông tin sách cần mượn.
#### Truy vấn tự động (bổ sung)
Được thực hiện trong lúc gõ tên hoặc mã sách.

---
## Trả sách
Vào: Mã sách.
Ra: Chuyển đã mượn thành có sẵn và hiển thị ra ngoài màn hình.
#### Truy vấn tự động (bổ sung)
Được thực hiện trong lúc gõ tên hoặc mã sách.

---
## Tính tiền phạt trả sách muộn
Vào: thông tin sách quá hạn. 
Ra: tổng tiền phạt.
#### Truy vấn tự động (bổ sung)
Được thực hiện trong lúc gõ tên hoặc mã sách.