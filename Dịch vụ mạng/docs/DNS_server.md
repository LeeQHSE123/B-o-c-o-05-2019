### DNS 
> DNS là viết tắt của Domain Name System (dịch phụ phân giải địa chỉ tên miền)
Phân giải tên miền thành địa chỉ IP 
(đặt địa chỉ IP tĩnh của máy chủ thành 2 địa chỉ vd: 8.8.8.8 và 8.8.4.4 thì mới run đc các packet DNS)

	
### Update trước khi cài đặt DNS để hệ thống tự tìm các gói bind phù hợp với phiên bản.
	`yum update`

### Cài đặt bind
	`yum install -y bind bind-utils`
- bind: gói tin (package) chính của DNS server
- bind-utils : Các tiện ích tích hợp cho DNS server
		