# LAB04 : Username enumeration via subtly different responses

**Đề bài:**

<img width="912" height="227" alt="image" src="https://github.com/user-attachments/assets/df203780-825b-405c-866a-d7127509173d" />
- Đề bài yêu cầu brute-force username và password

- Lấy gói POST login bất kì :
<img width="912" height="227" alt="image" src="https://github.com/user-attachments/assets/9816ccc3-19da-4b2a-8573-1abe4fae2052" />

- Chuyển qua Intruder và bắt đầu quét các username :
<img width="1678" height="1025" alt="image" src="https://github.com/user-attachments/assets/61fc9e01-2b68-4844-b70e-035c38603b36" />

- Sử dụng bộ lọc và loại bỏ hết các Response chứa : **Invalid username or password.**'
<img width="661" height="215" alt="image" src="https://github.com/user-attachments/assets/03a08bbb-b039-4061-bef6-fb07b342145a" />

- Ta tìm được username là : **app1**
<img width="1706" height="745" alt="image" src="https://github.com/user-attachments/assets/991d6caa-fa46-4398-a18f-bc642e5ea213" />

- Tiếp tục quay sang quét password :
<img width="1709" height="980" alt="image" src="https://github.com/user-attachments/assets/3d9d6c8b-9653-4234-a20d-504f462ddf01" />

- Ta có thể thấy với password là harley trang web trả về : 302 Found

- Ta đã tìm được username và password của người dùng nhờ brute-force và filter những thứ cấn thiết.
