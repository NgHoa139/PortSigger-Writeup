# LAB 03 : Inconsistent security controls

**Đề bài :**
<img width="895" height="85" alt="image" src="https://github.com/user-attachments/assets/bdcb9ce3-7fe1-4071-a148-308ce5a952eb" />

- Để giải bài thực hành, chúng ta cần truy cập vào bảng quản trị và xóa người dùng carlos.

- Chọn "Engagement tools" > "Discover content" để mở công cụ khám phá nội dung. Ta tìm thấy đường dẫn **/admin** :
<img width="989" height="714" alt="image" src="https://github.com/user-attachments/assets/9ee1cbdf-bbf2-470f-9b91-d3babbd38942" />

- Chuyển đường dẫn đến **/admin** cho biết chỉ có người dùng DontWannaCry được truy cập : 
<img width="1637" height="453" alt="image" src="https://github.com/user-attachments/assets/85e0edd4-69c3-4aa0-956d-4b31fcd68446" />

- Đăng kí tài khoản bằng email cho trước : 
<img width="753" height="466" alt="image" src="https://github.com/user-attachments/assets/ea8cf023-7ab6-42e4-8a32-d87d2d198950" />

- Sau khi đăng nhập ta có thể chỉnh sửa email của tài khoản : 
<img width="842" height="400" alt="image" src="https://github.com/user-attachments/assets/06da4c6e-2978-47b8-9a9b-0e3ae55b4ff6" />

- Sau khi update mail thành công ta có thể truy cập **Admin panel** :
<img width="1234" height="434" alt="image" src="https://github.com/user-attachments/assets/a95486fe-1f7e-40e5-ad77-8550aecdd288" />

- Ta xóa tài khoản **carlos** : 
<img width="1308" height="493" alt="image" src="https://github.com/user-attachments/assets/b578ce32-091a-4c74-93bf-030e643d0a99" />

- Nguyên nhân chính của lỗ hổng là logic kiểm soát truy cập được triển khai rời rạc, chỉ kiểm tra quyền ở một số chức năng hoặc giao diện, 
nhưng không áp dụng kiểm tra authorization đồng nhất cho toàn bộ API hoặc endpoint backend. 
