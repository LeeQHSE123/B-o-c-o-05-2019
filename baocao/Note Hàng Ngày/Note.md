﻿### Ngày 8 tháng 11 năm 2019

#### 1. Ảo hóa
##### Ảo hóa trên OS : Tài nguyên do OS cung cấp
##### Ảo hóa dưới OS : Ảo hóa luôn cả OS cung cấp tài nguyên . Các phần mềm hiện phổ biến  ISXY (bản cũ trước 5.5 thì free) | KMV (free) . 

#### 2. Init System
##### System V dùng cho bản CentOS 5 và Ubuntu 12
##### Upstart dung cho bản CentOS 6 và Ubuntu 14
##### Systemd dùng cho bản CentOS 7, 8 và Ubuntu 16.4 trở về sau

### 3. /var/tmp với /tmp
#### /var/tmp sẽ lưu dữ liệu tạm thời trong 30 ngày , và không bị mất khi reboot hệ thống
#### /tmp sẽ lưu trữ dữ liệu tạm thời trong 10 ngày  và sẽ bị xóa dữ liệu khi reboot lại hệ thống

### Ngày 12 tháng 11 năm 2019
### Master - Slave
- Check phân quyền (full quyền ) cho user được tạo từ Master và truy cập từ Slave.
- Truy cập remote từ Slave vào Master thêm -hIP , IP này là IP của master chứa DB. vd:` mysql -u username -p -h10.2.9.50 `.

### Ngày 18 tháng 11 năm 2019
### Keepalived
- `script trong vrrp_script`  : Dùng một đoạn script để check service coi có hoạt động không. Nếu hoạt động thì sẽ return 0 ngược lại sẽ return 1 . 

- `track_script` : sẽ nhận kết quả nhận được từ vrrp_script ,nếu sau 2 lần nó nhận được kết quả là 1(khác 0) thì nó sẽ xóa VIP khỏi card mạng con server hiện tại. Đổi trạng thái sang fault và VIP sẽ chuyển cho thằng khác.
