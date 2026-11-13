# BÁO CÁO: SO SÁNH TRADE-OFF CÁC GIẢI PHÁP VIẾT PROMPT

## Bước 1\. Đề xuất 2 prompt mẫu

Giải pháp 1: Prompt đơn giản, ngắn gọn

Prompt 1:

Hãy đóng vai giảng viên Tin học, trình bày ngắn gọn về cấu trúc Prompt tiêu chuẩn và các cách định dạng đầu ra như Few-shot, JSON và Table. Sử dụng ngôn ngữ dễ hiểu, có ví dụ minh họa và trình bày dưới dạng bảng.

Giải pháp 2: Prompt chi tiết, có nhiều ràng buộc

Prompt 2:

Bạn là giảng viên Tin học. Hãy giải thích chủ đề Cấu trúc Prompt tiêu chuẩn và Định dạng đầu ra cho sinh viên.

Yêu cầu:

* Sử dụng các thành phần của khung CREATE để xây dựng nội dung rõ ràng.  
* Giải thích Few-shot và đưa ra ít nhất 1 ví dụ mẫu.  
* Giải thích cách ép AI trả kết quả theo định dạng JSON và Table.  
* Ngôn ngữ đơn giản, ngắn gọn, phù hợp với sinh viên.  
* Không đưa thông tin ngoài chủ đề.  
* Không tự tạo dữ liệu khi đề bài chưa cung cấp.

Định dạng đầu ra: Chỉ trả về JSON hợp lệ theo cấu trúc:

{  
"khai\_niem": "Giải thích ngắn gọn",  
"few\_shot": {  
"muc\_dich": "Mục đích",  
"vi\_du": "Ví dụ minh họa"  
},  
"json": "Cách sử dụng và ví dụ",  
"table": "Cách sử dụng và ví dụ"  
}

Kiểm tra: Đảm bảo đủ các mục, không thiếu nội dung và JSON có cú pháp hợp lệ.

## Bước 2\. Bảng so sánh Trade-off

| Tiêu chí | Giải pháp 1 (Đơn giản) | Giải pháp 2 (Chi tiết) |
| ----- | ----- | ----- |
| Độ dễ hiểu | Cao | Trung bình |
| Tốn token | Ít | Nhiều hơn |
| Chặn lỗi biên | Trung bình | Rất tốt |
| Độ đầy đủ | Có thể thiếu ý | Đầy đủ hơn |
| Tính ổn định | Khá | Cao |
| Khả năng tái sử dụng | Thấp hơn | Cao |

## Bước 3\. Lựa chọn và chạy thử

Lựa chọn: Giải pháp 2\.

Lý do: Prompt 2 có yêu cầu cụ thể, có ví dụ và quy định định dạng đầu ra rõ ràng. Nhờ vậy, AI ít trả lời thiếu ý hoặc sai định dạng hơn. Mặc dù tốn nhiều token hơn nhưng kết quả ổn định và đầy đủ hơn.

Kết quả chạy thử Prompt 2:

```
{
  "khai_niem": "Prompt tiêu chuẩn là câu lệnh được xây dựng rõ ràng, có vai trò, bối cảnh, nhiệm vụ và định dạng đầu ra.",
  "few_shot": {
    "muc_dich": "Cung cấp ví dụ để AI hiểu cách trả lời mong muốn.",
    "vi_du": "Ví dụ: Đầu vào là Táo, đầu ra là Trái cây."
  },
  "json": "JSON giúp dữ liệu có cấu trúc rõ ràng, thuận tiện cho máy tính xử lý.",
  "table": "Table giúp trình bày thông tin thành hàng và cột, dễ đọc và so sánh."
}
```

