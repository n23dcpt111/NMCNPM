# Software Engineering Project – Document Management System

## 📌 Giới thiệu

Dự án này được phát triển trong môn Nhập môn Công nghệ Phần mềm.
Mục tiêu là áp dụng quy trình phát triển phần mềm, từ phân tích yêu cầu, thiết kế, lập trình, kiểm thử và triển khai.

## 🎯 Use Case chính

- Admin:
    + Đăng tải các tài liệu điện tử mới.
    + Cập nhật các tài liệu điện tử.
    + Đọc thông tin cá nhân của người dùng.
    + Tạo và xóa tài khoản.
    + Phân quyền tài khoản.
    + Chỉnh sửa thông tin cá nhân của người dùng.
    + Chỉnh sửa tài khoản của người dùng.
    + Phê duyệt các tài liệu điện tử của người dùng có tài khoản đăng tải.
- Người dùng khách:
    + Tìm kiếm tài liệu điện tử.
    + Xem trước tài liệu điện tử.
- Người dùng có tài khoản:
    + Tìm kiếm tài liệu điện tử.
    + Xem trước tài liệu điện tử.
    + Tải tài liệu điện tử.
    + Chỉnh sửa thông tin cá nhân.
    + Đổi mật khẩu.
    + Được hệ thống đề xuất thông minh các tài liệu điện tử.
    + Đăng tải các tài liệu điện tử
    + Xóa và chỉnh sửa các tài liệu điện tử của mình đăng tải.


![](image.png)


## 💻 Công nghệ sử dụng

- Ngôn ngữ: Java / Python / JavaScript / PHP
- IDE: Visual Studio Code
- CSDL: MySQL
- Quản lý phiên bản: Git + GitHub
- Mô hình phát triển: Agile – Scrum

## Use cases description:

a.	Thêm tài liệu:

•	Người thực hiện:  admin, người dùng
•	Mô tả: admin có thể thêm mới tài liệu vào hệ thống với các thông tin như tiêu đề, tác giả, tệp tài liệu. Người dùng có thể thêm tài liệu và gửi yêu cầu duyệt tài liệu, admin sẽ xem xét và duyệt tài liệu đó vào hệ thống.

1.	Người dùng truy cập vào hệ thống để thêm tài liệu
2.	Hệ thống yêu cầu người dùng đăng nhập
3.	Người dùng đăng nhập hệ thống
4.	Hệ thống kiểm tra các thông tin liên quan đến tài khoản người dùng này

    4.1 Nếu đúng, hệ thống hiển thị biểu mẫu cho người dùng nhập thông tin tài liệu gồm tiêu đề, tác giả, tệp tài liệu
        - Đối với thành viên, gửi yêu cầu thêm tài liệu để chờ admin duyệt tài liệu đó

            + Nếu tài liệu hợp lệ, tài liệu sẽ được thêm vào hệ thống và thông báo cho thành viên
            + Nếu không, admin sẽ từ chối và nhập lý do từ chối thông báo cho thành viên

        - Đối với admin, tài liệu sẽ được thêm trực tiếp vào hệ thống
        
    4.2 Nếu sai, hệ thống yêu cầu người dùng nhập lại tài khoản và mật khẩu


b.	Cập nhật thông tin tài liệu:

•	Người thực hiện:  admin, người dùng
•	Mô tả: admin có thể cập nhật tài liệu vào hệ thống. người dùng có thể cập nhật tài liệu của chính mình và gửi yêu cầu duyệt tài liệu, admin sẽ xem xét và duyệt tài liệu đó vào hệ thống.

1.	Người dùng truy cập vào hệ thống để cập nhật tài liệu
2.	Hệ thống yêu cầu người dùng đăng nhập
3.	Người dùng đăng nhập hệ thống
4.	Hệ thống kiểm tra các thông tin liên quan đến tài khoản người dùng này

    4.1 Nếu tài khoản là người dùng, hiển thị danh sách tài liệu của người dùng đó, người dùng chọn tài liệu và tiến hành cập nhật. Tài liệu sẽ chờ admin duyệt

        - Nếu tài liệu hợp lệ, tài liệu sẽ được cập nhật vào hệ thống và thông báo cho người dùng
        - Nếu không, admin sẽ từ chối và nhập lý do từ chối thông báo cho người dùng

    4.2 Nếu tài khoản là admin, hiển thị toàn bộ danh sách tài liệu, admin chọn tài liệu và cập nhật vào hệ thống

    4.3 Nếu sai, hệ thống yêu cầu người dùng nhập lại tài khoản và mật khẩu

c.	 Xóa tài liệu

•	Người thực hiện:  admin, người dùng
•	Mô tả: admin có thể xóa các tài liệu mong muốn, riêng người dùng chỉ được xóa tài liệu của chính mình.

    1.	Người dùng truy cập vào hệ thống để xóa tài liệu
    2.	Hệ thống yêu cầu người dùng đăng nhập
    3.	Người dùng đăng nhập hệ thống
    4.	Hệ thống kiểm tra các thông tin liên quan đến tài khoản người dùng này

        4.1 Nếu tài khoản là người dùng, hiển thị danh sách tài liệu của người dùng đó, người dùng chọn tài liệu và tiến hành xóa.
        4.2 Nếu tài khoản là admin, hiển thị toàn bộ danh sách tài liệu, admin chọn tài liệu và xóa vào hệ thống
        4.3 Nếu sai, hệ thống yêu cầu người dùng nhập lại tài khoản và mật khẩu
