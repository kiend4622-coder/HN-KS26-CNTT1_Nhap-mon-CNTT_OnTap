# BÀI LÀM – ÔN TẬP NGÀY 1

- **Họ tên:** Đỗ Trung Kiên
- **Lớp:** CNTT2
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Window 

## Phần A. Tổ chức thư mục bằng GUI

> Phần A được chấm qua kết quả B1 (tên thư mục gốc) và kết quả liệt kê toàn bộ dự án B8 ở Phần B, không cần ghi thêm ở đây.

- Thư mục gốc: `trung-tam-tieng-anh`
- Các thư mục con: `docs`, `media`, `data`, `logs`, `archive`
- Các file đổi tên snake_case:
  - `logo_trung_tam.png`
  - `anh_lop_hoc.jpg`
  - `lich_hoc.txt`
  - `hoc_vien_khoa_3.xlsx`
  - `access.log`
- File Excel nằm trong `data`
- File log nằm trong `logs`
- File `bai_lam_ngay1.md` ở thư mục gốc
- File `.env` vẫn ở thư mục gốc



## Phần B. Thao tác bằng CLI

### B1. Hiển thị đường dẫn tuyệt đối
pwd  
*Kết quả:*  
`/Users/kien/trung-tam-tieng-anh`

### B2. Liệt kê nội dung (kể cả file ẩn)
ls -a

### B3. Di chuyển file
mv lich_hoc.txt docs/  
mv logo_trung_tam.png media/  
mv anh_lop_hoc.jpg media/

### B4. Sao chép logo sang archive
cp media/logo_trung_tam.png archive/

### B5. Xoá 2 file .tmp
rm temp_201.tmp  
rm temp_202.tmp

### B6. Vào logs bằng đường dẫn tương đối, liệt kê, quay lại
cd logs  
ls  
cd ..

### B7. Thử thách – từ docs sao chép ảnh lớp học sang archive
cd docs  
cp ../media/anh_lop_hoc.jpg ../archive/  
cd ..

### B8. Liệt kê toàn bộ dự án kể cả file ẩn
ls -aR  
*Kết quả:*  
./
.env
bai_lam_ngay1.md
docs/
  lich_hoc.txt
media/
  logo_trung_tam.png
  anh_lop_hoc.jpg
data/
  hoc_vien_khoa_3.xlsx
logs/
  access.log
archive/
  logo_trung_tam.png
  anh_lop_hoc.jpg


### Các lệnh đã chạy (B1–B7)

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng

```

### Kết quả B1 (pwd)

```text
(Dán kết quả vào đây – xoá dòng này)

```

### Kết quả liệt kê toàn bộ dự án – B8 (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
(Dán kết quả vào đây – xoá dòng này)

```

## Tự chấm (điền sau khi có đáp án)

- **Điểm tự chấm:** ..../100
- **Lỗi mình đã mắc và cách sửa:**
