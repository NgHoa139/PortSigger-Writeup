 #LAB11 : Blind SQL injection with time delays

 Đề bài : 
 <img width="1094" height="337" alt="image" src="https://github.com/user-attachments/assets/6f732321-5c9d-45f9-9b6f-4c85b5d3578c" />

- Kiểm tra dữ liệu :
<img width="744" height="452" alt="image" src="https://github.com/user-attachments/assets/91430c4a-db03-41eb-8595-1ddc2194a2be" />

- Thay đổi TrackingID thành **TrackingId=x'||pg_sleep(10)--** để kết quả được phản hồi lại sau 10s
- Sau 10s thì trang web trả về kết quả :
<img width="1497" height="484" alt="image" src="https://github.com/user-attachments/assets/3bdeb870-94a2-4949-917f-143ce11d06be" />
