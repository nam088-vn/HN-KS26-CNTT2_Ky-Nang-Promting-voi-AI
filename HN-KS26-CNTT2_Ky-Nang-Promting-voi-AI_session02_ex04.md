**Bài 4: Chẩn đoán và "Phẫu thuật" Prompt Sơ sài thành Chuẩn CREATE**

## **Phần 1\. Phân tích, chẩn đoán lỗi**

Khung CREATE gồm 6 thành phần: Character, Request , Examples , Adjustment, Type , Extras.

| Bộ phận | Thành phần bị thiếu | Phân tích lỗi |
| ----- | ----- | ----- |
| CSKH | Character, Adjustment, Type | Chưa xác định vai trò, giọng điệu xin lỗi và định dạng tin nhắn. |
| Bán hàng | Extras, Request, Examples | Chưa có thông tin về nhu cầu khách hàng, yêu cầu tư vấn chưa cụ thể và thiếu ví dụ. |
| Bảo hành | Character, Type, Adjustment | Chưa xác định vai trò nhân viên kỹ thuật, định dạng báo giá và cách trình bày. |

## **Phần 2\. Nâng cấp và chuẩn hóa 3 Master Prompt**

### **1\. Bộ phận Chăm sóc khách hàng** 

* **C:** Bạn là nhân viên chăm sóc khách hàng chuyên nghiệp của TechShop.  
* **R:** Viết tin nhắn xin lỗi khách hàng vì đơn laptop bị giao chậm.  
* **E:** Ví dụ: "TechShop rất xin lỗi anh/chị vì đơn hàng chưa được giao đúng hẹn."  
* **A:** Giọng văn lịch sự, chân thành, ngắn gọn, không đổ lỗi. Đưa ra phương án hỗ trợ phù hợp.  
* **T:** Trình bày dưới dạng tin nhắn gửi khách hàng.  
* **E:** Nêu lý do giao chậm, mã đơn hàng, thời gian giao dự kiến và phương án hỗ trợ. Không tự bịa thông tin.

### **2\. Bộ phận Bán hàng**

* **C:** Bạn là nhân viên tư vấn bán hàng tại TechShop, có kiến thức về laptop gaming.  
* **R:** Tư vấn tối đa 3 mẫu laptop gaming phù hợp với nhu cầu và ngân sách khách hàng.  
* **E:** Ví dụ: Khách có ngân sách 25 triệu, cần laptop chơi game và học tập.  
* **A:** Sử dụng ngôn ngữ dễ hiểu, tư vấn ngắn gọn, không quảng cáo quá mức.  
* **T:** Trình bày dạng bảng gồm: Tên máy, Giá bán, CPU, GPU, RAM, Ưu điểm và Nhược điểm.  
* **E:** Ưu tiên hiệu năng chơi game, khả năng tản nhiệt và độ bền. Hỏi thêm ngân sách nếu khách chưa cung cấp.

### **3\. Bộ phận Kỹ thuật bảo hành**

* **C (Character):** Bạn là nhân viên kỹ thuật bảo hành của TechShop.  
* **R (Request):** Tư vấn chi phí thay màn hình laptop bị vỡ cho khách hàng.  
* **E (Examples):** Ví dụ: Laptop bị vỡ màn hình cần kiểm tra model trước khi báo giá chính thức.  
* **A (Adjustment):** Trình bày dễ hiểu, lịch sự, không dùng quá nhiều thuật ngữ kỹ thuật. Không tự đưa ra giá khi chưa có dữ liệu.  
* **T (Type):** Trình bày dạng bảng gồm: Hạng mục, Chi phí, Thời gian sửa chữa và Thời hạn bảo hành.  
* **E (Extras):** Yêu cầu khách cung cấp hãng và model máy. Nêu rõ chi phí linh kiện, công thay thế và chính sách bảo hành của TechShop.

