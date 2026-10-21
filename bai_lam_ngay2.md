BÀI LÀM – ÔN TẬP NGÀY 2
Họ tên: Đỗ TRung Kiên
Lớp: CNTT2
Link repository:
Hệ điều hành (Windows/macOS): Windows
Bài 1. Lọc log thủ công
Lệnh đã chạy
 Get-Content logs/access.log | Select-String "ERROR" > logs/error_report.txt
  Get-Content logs/error_report.txt
2 dòng lỗi đầu tiên trong error_report.txt
2025-10-18 08:17:59 [ERROR] Khong tim thay trang /lich-thi (404)
2025-10-18 08:25:55 [ERROR] Het thoi gian cho (timeout)
Bài 2. Đếm bằng pipeline
Lệnh
(Get-Content logs/access.log | Select-String "WARNING").Count
(Get-Content logs/payment.log | Select-String "ERROR").Count
Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)
WARNING trong access.log: 4
ERROR trong payment.log: 3
Bài 3. Chạy script auto_warning (.ps1 hoặc .sh)
Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\auto_warning.ps1
Nội dung file logs/warning_report.txt
Dang loc canh bao thanh toan...
Hoan thanh!

Bài 4. Báo cáo tổng hợp
Các lệnh đã chạy
"=== TONG HOP ACCESS LOG ===" > logs/tong_hop_ngay2.txt
Get-Content logs/access.log | Select-String "ERROR" >> logs/tong_hop_ngay2.txt
(Get-Content logs/payment.log | Select-String "WARNING").Count >> logs/tong_hop_ngay2.txt
Get-Content logs/tong_hop_ngay2.txt
Nội dung file logs/tong_hop_ngay2.txt
2025-10-18 08:17:59 [ERROR] Khong tim thay trang /lich-thi (404)
2025-10-18 08:25:55 [ERROR] Het thoi gian cho (timeout)
2025-10-18 08:33:51 [ERROR] Ket noi may chu du lieu that bai
2025-10-18 08:37:19 [ERROR] Ket noi may chu du lieu that bai
2025-10-18 08:49:43 [ERROR] Het thoi gian cho (timeout)
2025-10-18 08:53:11 [ERROR] Het thoi gian cho (timeout)
Bài 5. Câu hỏi ngắn
a) Lệnh > là ghi đè và xóa hết nội dung đã có trước đó của file ,còn lệnh >> là ghi tiếp nối vào nội dung của file trước đó mà không xóa nội dung cũ
b)Nếu dùng > thay cho >> thì ở lệnh đầu tiên sẽ bị xóa vĩnh viễn và bị ghi đè hoàn toàn bởi các dòng lỗi ERROR.
c)dùng đường dẫn tương đối logs/payment.log thay vì đường dẫn tuyệt đối như C:/Users/An/Desktop/... bởi vì đường dẫn tuyệt đối linh hoạt,có thể chạy ở những máy tính của người khá và để loại bỏ trường hợp không tìm thấy đường dẫ.
Tự chấm (điền sau khi có đáp án)
Điểm tự chấm: ..../100
Lỗi mình đã mắc và cách sửa: