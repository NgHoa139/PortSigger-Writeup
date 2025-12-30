# LAB03 : File path traversal, traversal sequences stripped non-recursively

**Đề bài:**
<img width="1121" height="225" alt="image" src="https://github.com/user-attachments/assets/f2d07114-dbd7-48fc-a977-b89ba866c923" />

- Từ đầu bài ta có thể đoán ra rằng chuỗi **../** có thể sẽ bị lọc ta thử **....//**
<img width="1492" height="381" alt="image" src="https://github.com/user-attachments/assets/664c6610-b3dd-4589-aa75-b011e7ce7cce" />

- Ta hoàn thành bài lab bởi vì lập trình viên lọc chuỗi sai cách
- Đầu vào : **....//....//....//etc/passwd**
- Sau khi bị lọc : **..//..//..//etc/passwd**
- Và hệ điều hành chuẩn hóa path : **..//**  thành  **../**
