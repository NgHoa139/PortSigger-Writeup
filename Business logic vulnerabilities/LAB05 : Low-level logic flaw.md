# LAB05 : Low-level logic flaw

**Đề bài :**

<img width="899" height="124" alt="image" src="https://github.com/user-attachments/assets/73a3ff7f-2f80-49aa-ae17-1d8d7128b1a3" />

- Đề bài khai thác một lỗi logic trong quy trình mua hàng của hệ thống để mua các mặt hàng với giá không mong muốn để mua một chiếc áo khoác.

- Sử dụng burp-suite để gửi request đặt áo khoác ta có thể thấy số tiền thanh toán đã bị tràn qua mức (2,147,483,647) và bắt đầu giá trị đã quay trở lại mức tối thiểu (-2,147,483,647) :
<img width="783" height="682" alt="image" src="https://github.com/user-attachments/assets/2fefa3f5-85fb-4c6b-ada9-b67092f4dbb8" />

- Ta có thể căn sao cho áo khoác vừa đủ để trả về số tiền có thể chấp nhận được để đặt hàng : 
<img width="765" height="710" alt="image" src="https://github.com/user-attachments/assets/200050d4-f49c-4158-8afd-123bb505227e" />

- Ta đặt số lượng lớn dẫn đến giá trị gây tràn số (integer overflow). Khi ta gửi request với giá trị số lượng vượt quá phạm vi mà hệ thống dự kiến, phép tính tổng giá trị đơn hàng có thể bị sai lệch
