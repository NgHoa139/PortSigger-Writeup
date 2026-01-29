# LAB03 : Password reset broken logic

**Đề bài:**
<img width="901" height="166" alt="image" src="https://github.com/user-attachments/assets/bfac3efb-1527-44ec-a1f2-067a5c7f1f5d" />

- Đề bài yêu cầu lấy lại mật khẩu của tài khoản **carlos**

- Ta lấy gói Request quên mật khẩu của tài khoản chính Wiener
<img width="1116" height="533" alt="image" src="https://github.com/user-attachments/assets/a13b036a-b948-4b74-867a-f1b7995da52e" />

- Xóa token và sửa username thành **Carlos**
<img width="1151" height="541" alt="image" src="https://github.com/user-attachments/assets/7a787eea-123e-4621-b650-9caeb7cafbb8" />

- Sau khi gửi Request thì trang web vẫn trả về trạng thái 302 nghĩa là ta đã đổi mật khẩu thành công
<img width="1300" height="608" alt="image" src="https://github.com/user-attachments/assets/318a3a22-94af-4527-a155-c583964167b4" />

- Ta đã hoàn thành bài lab bằng cách bypass chức năng lấy lại mật khẩu vì server không kiểm tra tính hợp lệ của reset
token và không xác minh token đó thuộc về tài khoản nào, cho phép ta không dùng token mà vẫn reset mật khẩu của người khác.
