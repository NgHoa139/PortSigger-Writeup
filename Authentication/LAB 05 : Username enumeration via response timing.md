# LAB 05 : Username enumeration via response timing

Đề bài : 
<img width="916" height="266" alt="image" src="https://github.com/user-attachments/assets/fb217328-9df0-42cc-bc1f-dbd787e74201" />

- Đề bài yêu cầu tìm 1 tài khoản dựa trên 1 tài khoản đã được cho trước

- Với các tài khoản sai username thì response sẽ rất nhanh khi nó không cần check đến password :
<img width="1587" height="893" alt="image" src="https://github.com/user-attachments/assets/80a0fa2f-be1d-489e-9164-d88133378778" />

- Đối với các tài khoản đúng username thì khi check password càng dài thời gian response càng lâu :
<img width="1581" height="890" alt="image" src="https://github.com/user-attachments/assets/57dd9c92-594f-40d3-aeb8-543224c8c342" />

- Nhưng khi đăng nhập sai quá nhiều thì máy chủ sẽ khóa đăng nhập của chúng ta trong 30 phút nên ta phải thêm : X-Forwarded-For vào để qua mặt được phần check IP của chúng ta

- Từ đó ta tận dụng thời gian response để tìm kiếm username bằng password dài :
<img width="1715" height="1021" alt="image" src="https://github.com/user-attachments/assets/7f678c8f-8ae5-4bb4-b66a-bd143b789c00" />

- Ta có thể thấy thời gian response của username = acid khá là dài nên đây sẽ là username đúng
- Ta tiếp tục quét password :
<img width="1717" height="1028" alt="image" src="https://github.com/user-attachments/assets/a0c0953d-0abf-43fd-9d23-5796fe97c1d9" />

- Ta thấy với password george thì trang web trả về 302 Found
  <img width="1717" height="1028" alt="image" src="https://github.com/user-attachments/assets/9d63f1af-1b52-47cf-a5ba-4fb1445f0c19" />

- Vậy ta đã tìm được username = acid và password = george
