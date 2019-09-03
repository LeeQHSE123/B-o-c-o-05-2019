### A.GIT.
> Git là một hệ thống quản lý phiên bản phân tán.
Git giống với các hệ thống quản lý phiên bản khác ở chỗ có ở chỗ Git hỗ trợ quả lý code và lịch sử thay đổi.
Ưu điểm của Git là git có khả năng phân nhánh, hỗ trợ rất tốt cho việc làm teamwork.


#### Các điểm nổi bật của GIT
#### 1. Sắp xếp công việc tốt hơn : 
- Do git có khả năng phân nhánh nên sẽ chia cv thành các task để ta có thể tập chung vào tốt hơn.
#### 2.Linh hoạt hơn khi phải làm cùng nhiều task một lúc.
- Các task có thể làm việc độc lập với nhau.
#### 3.Tự tin khi thử nghiệm ý tưởng mới 
- Có thể kiểm thử nhiều lần trước khi update vào dự án.
		
		
### B. GIT-about
> Git coi dữ liệu của mình như một tập hợp các ảnh "snapshot" của hệ thống tập tin.
Mỗi lần lưu trạng thái mới Git sẽ "chụp ảnh" toàn bộ nội dung trong hệ thống tập tin.
Nếu tập tin nào không thay đổi thì git chỉ lưu đường dẫn tới tập tin gốc trước đó.


- Repository : Kho chứa toàn bộ các project , cac source code  và nội dung thay đổi file và người thay đổi các file đó.
	- Repository sẽ gồm 2 loại : Remote repository ==> chia sẻ với nhiều người và đặt trên server.
	- Local repository ==> đặt tại máy tính các nhân 
	
- Branch là một nhánh của repository. Các branch sẽ hoạt động độc lập với nhau và phát triển một tính năng không gây ảnh hưởng tới các nhánh khác.
Các nhánh hợp lại cùng nhau gọi là merge ( hợp nhất). Nhánh mặc định sẽ là master
Một branch trên local có thể liên kết với 1 hoặc nhiều thậm trí la không nhánh nào trên remote.
		
- Backup git:
Sao lưu toàn bộ dữ liệu từ máy chủ về máy tính cá nhân (clone) và được ( push ) lên để thay thế máy chủ chính hay 
( pull) cập nhật liên tục các thay đổi của máy chủ.
		
		
### C.Cơ chế hoạt động của git:
- Các file khi được clone về từ server sẽ được lưu ở trong  Working directory 
- Các file được sủa hay bổ xung cập nhật sẽ được lưu trong Staging area
- Cuối cùng các file sau khi commit sẽ được lưu vào cùng Repository
		
- Push để đẩy các commit lên server 
- Tiếp tục thì sẽ pull  và push lên server để làm việc chung.
		
### D.Thực hành.

		Clone từ repository từ server về máy 
			git clone đường dẫn clone server 
		Kiểm tra trạng thái của git trong working directory:
			git status
		Thêm vào vùng staging are 
			git add ten file || git add .      : add tất cả các thay đổi
		Thêm commit 
			git commit -m "ghi chú" 
			
		Xem lịch sử commit 
			git log
		
		Đẩy lên remote repository
			git push 
		Coi đã thay đổi những gì trong working area
			git diff
		Cập nhật những thay dổi mới nhất từ remote về local
			git pull 
		
		
		
	Đưa file lên github.
		Tạo file README 
			echo "# demo" >> README.md
		Khởi tạo repository local
			git init
		Connect với remote repository
			git remote add origin https://github.com/LeeQHSE123/demo.git
		Đẩy lên remote repo
			git push -u origin master

	Tạo branch mới	
		git checkout -b tên nhánh mới 
	Truy cập vào nhánh nào đó
		git checkout tên nhánh 
	Push branch mới lên remote repo 
		git push origin tên nhánh 
	Xem toàn bộ các cập nhật 
		git log --online --graph --decorate --all
	Gộp nhánh ( cập nhật)
		git merge tên nhanh 
		
	Liệt kê các branch trong repo 
		git branch 
	Xóa một branch
		git checkout -d tên nhánh 
		
	Phân biệt git pull và git fetch
		git pull sẽ cập nhật thay đổi từ remote về local và đồng bộ hóa các source code 
		git fetch thì cập nhật metadata ( git remote có những branch nào và có những thay đổi nào từ remote mà local chưa được cập nhật ).
		
		
		
		
		
		