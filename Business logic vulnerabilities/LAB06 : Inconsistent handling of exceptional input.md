# LAB06 : Inconsistent handling of exceptional input

**Đề bài :**
<img width="892" height="107" alt="image" src="https://github.com/user-attachments/assets/9da2b0c3-d0cb-4235-b1ac-ad44364e0505" />

- Đề bài yêu cầu truy cập vào bảng quản trị và xóa người dùng Carlos.

- Sử dụng Content Discovery trên Burp-Suite để khám phá các đường dẫn ta thấy có **/admin** : 
<img width="994" height="712" alt="image" src="https://github.com/user-attachments/assets/5b532d7a-a8b5-47bc-ab6c-2d2238a2e741" />

- Truy cập vào thì ta biết chỉ có DontWannaCry user mới truy cập được  : 
<img width="1212" height="254" alt="image" src="https://github.com/user-attachments/assets/ed7eb8b9-6946-408c-8641-f8c9d4c33a95" />

- Đăng kí tài khoản với email dài và khi đăng nhập vào thì bị cắt xuống còn 255 kí tự :
<img width="1232" height="257" alt="image" src="https://github.com/user-attachments/assets/b629ca45-1347-4ae6-a737-de9bc7eb8d4b" />

- Điều này cho tháy ta có thể chèn **dontwannacry.com** vào phần mail và căn chỉnh sao cho số lượng ký tự phù hợp để chữ "m" ở cuối @dontwannacry.com chính xác là ký tự thứ 255 :
<img width="834" height="488" alt="image" src="https://github.com/user-attachments/assets/9d1c25a4-8aba-443a-9766-c978d8d7e131" />

- Sau khi xác thực đăng nhập vào ta được :
<img width="1294" height="309" alt="image" src="https://github.com/user-attachments/assets/249c55a8-0ba9-42cc-9d7e-6b5ba9d786ea" />

- Sau khi bị cắt còn 255 kí tựu thì ta có địa chỉ mail là **@dontwannacry.com** và ta có thể xâm nhập vào **Admin panel** để xóa người dùng : 
<img width="1206" height="240" alt="image" src="https://github.com/user-attachments/assets/dcb48009-4c0b-46e8-8364-d6e8d8fccc5c" />

- Ta truy cập được vào Admin panel bởi vì đầu vào của mail không được chuẩn hóa và cắt bỏ phần thừa sau kí tự thứ 255 nên ta có thể chèn mã độc hoặc lợi dụng để truy cập trái phép vào
trang bằng quyền hạn Admin.
