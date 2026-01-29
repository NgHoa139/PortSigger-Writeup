# LAB02 : 2FA simple bypass

**Đề bài:**
<img width="895" height="197" alt="image" src="https://github.com/user-attachments/assets/12ab36aa-184e-47fb-b498-3ce45eeef0e2" />

- Đề bài yêu cầu vượt qua xác thực 2 yếu tố
- Đăng nhập vào tài khoản của mình và xác thực 2 yếu tố
<img width="811" height="500" alt="image" src="https://github.com/user-attachments/assets/89ebe937-e827-4160-8344-6054d33f05ff" />
<img width="755" height="539" alt="image" src="https://github.com/user-attachments/assets/99df2cde-cc17-4c56-b4ba-feaef11369ed" />

- Đăng xuất và đăng nhập vào tài khoản cần xác thực
<img width="760" height="427" alt="image" src="https://github.com/user-attachments/assets/32597207-fbac-4f72-860b-cbe4454be018" />

- Ở phần login2 này ta thay bằng my-account để bypass
<img width="814" height="662" alt="image" src="https://github.com/user-attachments/assets/3978ba5d-d8d5-49f6-a14e-1b504c49642c" />

- Khi nhập /my-account server tin rằng bạn đã đăng nhập xong, nên cho vào luôn. Bypass được 2FA vì server chỉ kiểm tra session đăng nhập mà không kiểm tra trạng thái hoàn thành 2FA.
