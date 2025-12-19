#SQL injection attack, querying the database type and version on Oracle

Đề bài : <img width="1030" height="115" alt="image" src="https://github.com/user-attachments/assets/137c8b8f-dea4-4130-9e54-3a63ef64bd8d" />

- Truy cập trang web ta thấy có 2 cột chính là tiêu đề(được in đậm) và mô tả 
<img width="1155" height="911" alt="image" src="https://github.com/user-attachments/assets/3cf9d327-879d-4dee-a7f9-3fb83e7596dd" />

- Kiểm tra trên Burp Suite
<img width="1533" height="130" alt="image" src="https://github.com/user-attachments/assets/8cfda040-a04a-4cb8-9807-a50ad6760a38" />
<img width="1526" height="139" alt="image" src="https://github.com/user-attachments/assets/7d719024-8b0f-4fe1-9fd1-4d65a8891932" />
<img width="1533" height="160" alt="image" src="https://github.com/user-attachments/assets/3fb5e4e5-9402-44cf-a936-6a6735978cd9" />

- Chúng ta có thể biết chắc rằng query gốc chỉ có 2 cột

- Từ hint ta biết bảng này thuộc Oracle databases nên ta có thể tấn công vào bảng có sẵn trong Oracle databases là bảng DUAL xem
  bảng có trả về hai cột không
<img width="1536" height="201" alt="image" src="https://github.com/user-attachments/assets/74f2bc1c-88a4-48fd-87d3-5e3a481468b3" />


- Ta tấn công vào v$version để khiến SQL trả về thêm version của hệ thống :
  <img width="1531" height="605" alt="image" src="https://github.com/user-attachments/assets/eb63b12c-99a4-4292-9b1f-4b5a2520326e" />

- Ta đã hoàn thành bài LAB nhờ UNION câu lệnh kết hợp các bảng để hiển thị ra version của hệ thống!!
