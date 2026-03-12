# LAB04 : Flawed enforcement of business rules.md

**Đề bài :**

<img width="882" height="134" alt="image" src="https://github.com/user-attachments/assets/fe8efb00-398d-4d23-bafb-55f0176765f1" />

- Đề bài yêu cầu mua Lightweight l33t leather jacket

- Khi đăng nhập vào và kiểm tra ở cuối trang ta thấy có thêm mã giảm giá khi điền mail :
<img width="1204" height="573" alt="image" src="https://github.com/user-attachments/assets/97d793d7-4b74-4c09-8ec4-a0cedf22891c" />
<img width="461" height="174" alt="image" src="https://github.com/user-attachments/assets/f57120e0-ef8a-41b6-81b9-443175fb519f" />

- Áp dụng mã nhiều hơn một lần : 
<img width="735" height="895" alt="image" src="https://github.com/user-attachments/assets/ae65feb5-73c5-414c-a8a9-a0b10e842023" />

- Ta đã có thể mua 1 cái áo bằng cách áp mã giảm giá nhiều lần. Nếu nhập 2 mã gần nhau thì sẽ báo trùng mã và không sử dụng được nhưng ta có thể nhập luân phiên các mã với nhau.
- Nguyên nhân cốt lõi của lỗ hổng là thiết kế logic nghiệp vụ không tính đến các trường hợp lạm dụng (abuse cases).
Khi attacker gửi các request thủ công thông qua proxy như Burp Suite, họ có thể thay đổi thứ tự thao tác hoặc lặp lại hành động để phá vỡ các giả định của hệ thống.
- Điều này xảy ra vì hệ thống không kiểm tra trạng thái giao dịch hoặc điều kiện sử dụng khuyến mãi một cách nhất quán ở backend, mà chỉ dựa vào các giả định về cách người dùng tương tác hợp lệ với giao diện.
