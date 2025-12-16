# PortSigger-Writeup
1. SQL injection vulnerability in WHERE clause allowing retrieval of hidden
   
   Đề bài : <img width="1041" height="153" alt="image" src="https://github.com/user-attachments/assets/2cf1a276-e1fd-4cda-8316-785410edad96" />

     Truy cập vào trang web sẽ hiện :
 <img width="1146" height="948" alt="image" src="https://github.com/user-attachments/assets/91601566-8f8f-41b8-a45e-ce9f59dd433e" />
     Khi sử dụng thanh tìm kiếm địa chỉ trang web sẽ hiện : <img width="144" height="32" alt="image" src="https://github.com/user-attachments/assets/02d35f67-606f-4916-9682-efb4a348399e"

   Ta sẽ có câu lệnh như ở đầu bài : SELECT * FROM products WHERE category = 'Gifts' AND released = 1 . Vậy điều gì sẽ xảy ra nếu ta thay Gifts bằng ' OR 1=1--  để bypass điều kiện truy vấn trong SQL

   Thay lệnh : <img width="230" height="36" alt="image" src="https://github.com/user-attachments/assets/addc7901-d2de-402e-af19-302e6075830d" />  có nghĩa là : SELECT * FROM products WHERE category = '' OR 1=1-- ' AND released = 1

   Ta đã hoàn thành bài lab nhờ cách bypass qua câu lệnh truy vấn của SQL nhờ OR 1=1-- <img width="1163" height="949" alt="image" src="https://github.com/user-attachments/assets/7648fcfc-bc92-4f15-a907-7c7bd81f7af3" />


   Lí do : Câu lệnh truy vấn OR của SQL sẽ đúng khi 1 trong 2 điều kiện đúng mà chúng ta đã thêm điều kiện luôn đúng là 1=1 nên câu lệnh Where sẽ luôn trả về kết quả đúng.
   Còn -- trong SQL là lệnh comment dùng để xóa bỏ phần truy vấn đằng sau nhằm bypass dẽ dàng hơn

