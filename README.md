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

- ![15](https://github.com/user-attachments/assets/6c242ca5-6516-44b4-927f-569c800bdc31)


- Viết chương trình C/C++ có sử dụng thư viện đã tạo
  
- ![16](https://github.com/user-attachments/assets/7025d1e9-bff5-4b3a-b47e-70f5e6144c08)


- Biên dịch chương trình với 2 loại thư viện (Thư viện tĩnh và Thư viện động) thành 2 chương trình.

- ![17](https://github.com/user-attachments/assets/3874ac00-d429-463f-8619-882e22f024fd)
- ![18](https://github.com/user-attachments/assets/75fcac5f-f23a-444d-890d-ee67d63b0b05)


- Đưa chương trình và thư viện đã biên dịch xuống BBB (Cả 2 chương trình) thử nghiệm hoạt động.

đưa static xuống BBB và hoạt đọng được
- ![19](https://github.com/user-attachments/assets/89e32da5-6b1a-46c7-baac-10cc2093ee2f)

đưa dynamic xuống BBB và hoạt động được
- ![20](https://github.com/user-attachments/assets/12aa6ee6-a39d-4a26-a9a4-ddc67e14b6be)


- So sánh về kích thước của 2 chương trình đã tạo ở bước (5) về dung lượng, yêu cầu phụ thuộc (sử dụng lệnh readelf dependencies).
  trên lý thuyết là thư viện tĩnh sẽ nặng hơn nhưng 2 file này  lại có kích thước như nhau bởi vì hàm rất rất nhỏ, 7.8K thực chất là bộ khung của hđh và thư viện stdio.h nên không tạo ra được sự khác biệt về mặt trực quan
  Dùng 2 lệnh trên sẽ thấy rõ sự khác biệt trong 2file
  
- Bài tập 03: Tích hợp ứng dụng và thư viện và Buildroot

Yêu cầu: Xây dựng chương trình có phụ thuộc vào cả 2 thư viện ở Bài 1 và Bài 2 vào Buildroot có ràng buộc phụ thuộc.

- Đưa thư viện ở bài 2 vào Buildroot và biên dịch tích hợp thành công
.
  Tạo file cấu hình giao diện
  ![21](https://github.com/user-attachments/assets/12223170-4ac5-46db-b0f6-733ee310a8ec)
  
  Tạo file luật biên dịchmymath.mk
  ![22](https://github.com/user-attachments/assets/d2cf3b46-8a57-449b-8b64-7b4733684c77)

  Đăng ký gói mymath với Buildroot
  ![23](https://github.com/user-attachments/assets/2392c98e-8721-4b36-af77-b026200cae6d)
  ![24](https://github.com/user-attachments/assets/934e3482-ad23-4f0d-80d2-750e73d65474)


- Viết 01 chương trình C/C++ có sử dụng cả 2 thư viện ở bài 01 và bài 02.

- Biên dịch thành công chương trình và chạy thành công trên BBB
  
![25](https://github.com/user-attachments/assets/e7cb78ef-e209-4547-b1ff-8b324a3f5eda)

- Viết cấu hình cho chương trình trên Buildroot, chú ý kèm điều kiện phụ thuộc vào 02 thư viện đã nêu. (Khi bật (enable) chương trình này, CJSON và thư viện tùy chỉnh tự động được kích hoạt).
  
![26](https://github.com/user-attachments/assets/1f498612-d138-4062-a48c-9a2edcdabdca)

- Biên dịch lại Buildroot, cài đặt và khởi chạy chương trình thành công trên BBB ngay sau khi cài đặt.
  
![27](https://github.com/user-attachments/assets/ca4ede17-9f19-4530-abfd-376be27ec7c4)
