Bài 6: Loại bỏ "Lời chào vô nghĩa" bằng Kỹ thuật Structured Output

## Phần 1\. Phân tích nguyên nhân lỗi

AI thường tự động thêm lời chào và lời chúc vì:

Thói quen giao tiếp: AI được huấn luyện để trả lời thân thiện, lịch sự như con người.

Thiếu ràng buộc: Prompt chưa yêu cầu AI chỉ trả về JSON, nên AI tự thêm lời giới thiệu và kết luận.

Hiểu chưa đúng yêu cầu: AI xem JSON là nội dung cần trình bày chứ không phải định dạng duy nhất được phép trả về.

Hậu quả: Backend đọc ký tự đầu tiên là chữ "D" thay vì dấu `{`, khiến lệnh JSON.parse bị lỗi.

## Phần 2\. Hoàn thiện Prompt ép cấu trúc

Prompt đề xuất:

Bạn là hệ thống xử lý dữ liệu bảo hành của TechShop. Nhiệm vụ của bạn là đọc biên bản bảo hành và chuyển thông tin thành JSON.

Yêu cầu bắt buộc:

1. Chỉ trả về một chuỗi JSON hợp lệ.  
2. Không viết lời chào, lời cảm ơn, lời chúc hoặc giải thích.  
3. Không sử dụng Markdown hoặc dấu \`\`\` để bao quanh JSON.  
4. Không thêm bất kỳ nội dung nào trước hoặc sau JSON.  
5. Phải bắt đầu bằng ký tự `{` và kết thúc bằng ký tự `}`.  
6. Chỉ sử dụng đúng 3 trường: `customer_name`, `device`, `issue`.  
7. Nếu thiếu thông tin, điền giá trị `null`, không tự suy đoán.  
8. Sử dụng dấu ngoặc kép cho tên trường và giá trị dạng chuỗi. Không thêm dấu phẩy ở cuối.

