# **Bài 5: Cơ chế In-Context Learning trong Phân loại Review Khách hàng**

## Phần 1\. Phân tích cơ chế In-Context Learning

In-Context Learning hay còn được viết tắt ICL: là cách giúp AI học cách trả lời thông qua các ví dụ được đưa trực tiếp vào Prompt mà không cần huấn luyện lại mô hình.

Cơ chế hoạt động:

Bước 1: Cung cấp cho AI một số ví dụ đánh giá và kết quả phân loại.

Bước 2: AI nhận ra từ mỉa mai, khen đểu và ý nghĩa thực sự của câu nói.

Bước 3: Khi gặp đánh giá mới, AI dựa vào các ví dụ đã cho để phân loại chính xác hơn.

Ví dụ: Câu nói "Pin trâu thật, dùng được 30 phút đã hết" có vẻ đang khen nhưng thực chất là chê.

ICL giúp AI hiểu ngữ cảnh ngay trong câu lệnh, không cần train lại model.

## Phần 2\. Sửa lỗi bằng Few-shot

Prompt Few-shot hoàn chỉnh:

Bạn là nhân viên kiểm tra chất lượng của TechShop. Hãy phân loại đánh giá sản phẩm thành 2 loại: TÍCH CỰC hoặc TIÊU CỰC.

Hãy chú ý những câu nói mỉa mai, khen đểu. Không chỉ dựa vào những từ ngữ khen như "đẹp", "tốt", "tuyệt vời" mà phải hiểu ý nghĩa thực sự của cả câu.

3 ví dụ 

Ví dụ 1 – Nhiệt độ:

* Input: "Máy mát thật, chơi game 15 phút mà CPU lên 98 độ C, đúng là máy sưởi mini\!"  
* Output: TIÊU CỰC → chê máy nóng nhanh

Ví dụ 2 – Pin:

* Input: "Pin trâu ghê, vừa rút sạc dùng được 30 phút đã phải cắm lại\!"  
* Output: TIÊU CỰC → chê máy pin yếu

Ví dụ 3 – Giao hàng:

* Input: "Giao hàng nhanh thật, đặt từ đầu tuần mà cuối tháng mới nhận được\!"  
* Output: TIÊU CỰC → chê hàng giao chậm