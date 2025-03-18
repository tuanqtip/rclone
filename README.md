# Hướng dẫn rclone

## Lệnh vào rclone
rclone config

## Chọn new remote:
n -> Enter

## Đặt tên remote:
Remote01 -> Enter

## Chọn mã hóa
crypt -> Enter

## Nhập đường dẫn folder mã hóa (folder này đã có dữ liệu mã hóa, hoặc ko có dữ liệu nào cả)
C:\Users\tuan.pa\Desktop\Data_Encrypted

## Chọn các phương thức mã hóa file, folder, và mật khẩu (Nếu giải mã dữ liệu folder thì cần nhập đúng các thông tin Remote đã cấu hình cho folder mã hóa đó)
1 -> Enter
1 -> Enter
...

## Moun Remote01: tạo ra 1 folder ảo chứa dữ liệu được mã hóa (Data_Decrypt)
rclone mount Remote01: C:\Users\tuan.pa\Desktop\Data_Decrypt --vfs-cache-mode writes --links

## Hoặc chuyển dữ liệu mã hóa thành dữ liệu giải mã đến 1 folder thật mới
rclone copy Remote01: C:\Users\tuan.pa\Desktop\GiaiMa --progress

