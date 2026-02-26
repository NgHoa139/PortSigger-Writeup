# LAB01 : Excessive trust in client-side controls

Đề bài : 
<img width="889" height="126" alt="image" src="https://github.com/user-attachments/assets/b133c09d-1e3e-43d0-9803-e1eab46132ab" />

- Đề bài yêu cầu mua những đồ đã được yêu cầu

- Đầu tiên ta lấy gói Request khi thêm sản phẩm vào giỏ hàng
<img width="1544" height="501" alt="image" src="https://github.com/user-attachments/assets/ca80daba-4625-4566-820c-0aa130f72f15" />

- Ta sửa giá thành 1 và ta có thể thấy trong giỏ hàng là sản phẩm được yêu cầu với giá là 1
<img width="735" height="599" alt="image" src="https://github.com/user-attachments/assets/2b4b635f-87a0-4f6e-9361-4e7e47cfc2e8" />

- Ta đã khai thác thành công lỗ hổng vì server tin tưởng tuyệt đối vào input của người dùng thay vì tự mình xác thực dữ liệu nhạy cảm (giá tiền) ở phía backend.
