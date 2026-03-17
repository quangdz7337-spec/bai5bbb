# bai5
- Bài tập 01: Biên dịch ứng dụng với thư viện đã có

- Yêu cầu: Viết 01 chương trình C/C++ có sử dụng thư viện cJSON.
- Bật cJSON trong Buildroot và build lại OS tích hợp thư viện cJSON
- ![8](https://github.com/user-attachments/assets/73ade652-88ed-4a2c-8f0d-02b00a5ecba0)

- Viết chương trình C/C++ có sử dụng thư viện cJSON thực hiện parse 01 gói tin JSON thành các trường thông tin và in lên Terminal.
-  ![9](https://github.com/user-attachments/assets/0a7fc66d-fca6-4fbc-859a-778814b98f17)

- Thực hiện biên dịch chéo sử dụng Toolchain đã cập nhật ở bước 1 (VD: Tên là HelloJSON.c)

- Biên dịch thành công chương trình HelloJSON.c và đưa xuống BBB.

- ![10](https://github.com/user-attachments/assets/c20465e6-bcc4-4bfd-9eb8-4e3b1d8a893a)

- ![11](https://github.com/user-attachments/assets/2922a621-fe32-4095-a7e9-654d2b84bbef)
  
- Khởi chạy thành công chương trình đã biên dịch.
  
- ![12](https://github.com/user-attachments/assets/2d6fa814-841b-4d11-ab6d-14237b8466ac)
  
- Bài tập 02: Tự tạo thư viện cá nhân

- Yêu cầu: Tự tạo 01 thư viện đơn giản của riêng mình và ứng dụng sử dụng thư viện đó

- Viết 01 thư viện đơn giản gồm 01 file .h và 01 file .c thực hiện 1 nhiệm vụ đơn giản như: Cộng 2 số, Tìm số nguyên tố.... (tùy ý).
  
- ![13](https://github.com/user-attachments/assets/2c11c106-2cbc-4ec7-abce-298859c5793b)


- Biên dịch thành công thư viện ở bước 1 thành: Static Library (.a) và Dynamic Library (.so)

- ![14](https://github.com/user-attachments/assets/6d4431ad-a46b-4f2f-817c-288c4d5f1d24)


- Đưa thư viện đã biên dịch thành công ở bước 2 vào Sysroot.

- Viết chương trình C/C++ có sử dụng thư viện đã tạo

- Biên dịch chương trình với 2 loại thư viện (Thư viện tĩnh và Thư viện động) thành 2 chương trình.

- Đưa chương trình và thư viện đã biên dịch xuống BBB (Cả 2 chương trình) thử nghiệm hoạt động.

- So sánh về kích thước của 2 chương trình đã tạo ở bước (5) về dung lượng, yêu cầu phụ thuộc (sử dụng lệnh readelf dependencies).
