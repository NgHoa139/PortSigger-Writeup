# LAB01 : Username enumeration via different responses.md

**Đề bài:**

<img width="907" height="230" alt="image" src="https://github.com/user-attachments/assets/e9298ef5-a6f8-4825-bbd8-23a55c42d2ae" />

- Bài lab yêu cầu chúng ta tấn công brute-force tên đăng nhập và mật khẩu của người dùng ở trên page
- Đăng nhập thử để lấy gói Request và chuyển qua Intruder
<img width="1357" height="537" alt="image" src="https://github.com/user-attachments/assets/4a53e103-bb68-4a87-94bc-0c624f1fc86f" />

- Ta quét tài khoản trước :
<img width="521" height="901" alt="image" src="https://github.com/user-attachments/assets/139f28dc-1ae7-44f3-80b7-5c14b54dfc3c" />

- Ta thấy username **as400** trả lại length khác với toàn bộ số còn lại là : Incorrect password
<img width="1632" height="759" alt="image" src="https://github.com/user-attachments/assets/d19f4c85-627a-42d5-b759-32da9e98b7ab" />

- Tiếp tục sử dụng username **as400** và ta brute-force password
<img width="1394" height="766" alt="image" src="https://github.com/user-attachments/assets/d081f6cc-0e19-49b6-9aac-3f179ef32560" />

- Ta thấy password là : **amanda** trả về Status code là 302 có nghĩa là đã đăng nhập thành công
- Ta đã hoàn thành bài lab và tìm được username với password bằng cách brute-force.
