### Các tham số trong ./configure
- ` --help ` : các message gợi ý , trợ giúp

- ` --prefix=path ` : Chỉ định thư mục chứa tập tin cấu hình , đồng thời chứa đường dẫn thư viện 	( Thư mục mặc định là : / usr / local / nginx ).

- ` --sbin-path=path ` : Nơi chứa thư mục thực thi NGINX ( Thư mục mặc định là : prefix/sbin/nginx. )
- ` --modules-path=path ` : Định nghĩa thư mục , nơi các Module sẽ được cài đặt.
- ` --conf-path=path ` : Nơi chứa tập tin cấu hình nginx.conf . ( Thư mục mặc định là : prefix/conf/nginx.conf )
- ` --error-log-path=path `: Nơi lưu nhật kí các lỗi , các cảnh báo ( Thư mục mặc định prefix/logs/error.log.) 
- ` --pid-path=path ` : Nơi lưu dữ các ID tiến trình của quy trình chính . Sau khi cài đặt tệp trên có thể thay đổi trong file cấu hình nginx.conf bằng lệnh pid. (Nơi lưu trữ mặc định là : prefix/logs/nginx.pid.)

` --lock-path=path ` : Nơi lưu trữ các tệp khóa . Sau khi cài đặt, có thể thay đổi giá trị trong tập tin cấu hình nginx.conf bằng lệnh lock_file . (Nơi lưu trữ mặc định là : prefix/logs/nginx.lock.)

` --user=name  && --group=name `:Thiết lập tên và nhóm người dùng (không cần đặc quyền) được sử dụng bởi Nginx worker processes (Để vận hành máy móc thì cần công nhân vận hành, worker processes có thể hiểu trong trường hợp này là như thế).  

` --build=name ` : Đặt tên xây dựng Nginx tùy chọn.

` --builddir=path ` : Thiết lập một thư mục xây dựng.

` --with-select_module && --without-select_module ` : Cho phép hoặc vô hiệu hóa build các module với phương thức select().
Mô-đun này được xây dựng tự động nếu nền tảng không xuất hiện để hỗ trợ các phương thức phù hợp hơn như kqueue, epoll hoặc / dev / poll.

` --with-poll_module && --without-poll_module ` : Cho phép hoặc vô hiệu hóa  build các module với phương thức poll(). . Mô-đun này được xây dựng tự động nếu nền tảng không xuất hiện để hỗ trợ các phương thức phù hợp hơn như kqueue, epoll hoặc / dev / poll.

` --with-threads ` : Cho phép sử dụng các thread pools ( nhóm luồng)

` --with-file-aio ` : Cho phép sử dụng tệp I / O không đồng bộ (AIO) trên FreeBSD và Linux.

` --with-http_ssl_module ` : Xây dựng module bổ xung hỗ trợ cho giao thức HTTP. Cần có thư viện OpenSSL để xây dựng và thực hiện module này.

` --with-http_v2_module ` : Cho phép xây dựng một mô-đun cung cấp hỗ trợ cho HTTP / 2. Modul này không được xây dựng theo mặc định.

` --with-http_realip_module ` : Cho phép xây dựng mô đun ngx_http_realip_module thay đổi địa chỉ máy khách thành địa chỉ được gửi trong trường tiêu đề đã chỉ định. Mô-đun này không được xây dựng theo mặc định. 

` --with-http_addition_module `: Cho phép xây dựng mô-đun ngx_http_addition_module thêm văn bản trước và sau khi phản hồi. Mô-đun này không được xây dựng theo mặc định.

` --with-http_xslt_module && --with-http_xslt_module=dynamic `: Cho phép xây dựng mô đun ngx_http_xslt_module để chuyển đổi các phản hồi XML bằng cách sử dụng một hoặc nhiều biểu định kiểu XSLT. Mô-đun này không được xây dựng theo mặc định. Các thư viện libxml2 và libxslt được yêu cầu để xây dựng và chạy mô-đun này.

` --with-http_image_filter_module && --with-http_image_filter_module=dynamic ` : Cho phép xây dựng mô-đun ngx_http_image_filter_module để chuyển đổi hình ảnh ở định dạng JPEG, GIF, PNG và WebP. Mô-đun này không được xây dựng theo mặc định.

` --with-http_sub_module `: Cho phép xây dựng mô-đun ngx_http_sub_module sửa đổi phản hồi bằng cách thay thế một chuỗi được chỉ định bằng một chuỗi khác. Mô-đun này không được xây dựng theo mặc định.

` --with-http_geoip_module && --with-http_geoip_module=dynamic ` : Cho phép xây dựng mô đun ngx_http_geoip_module tạo các biến tùy thuộc vào địa chỉ IP của máy khách và cơ sở dữ liệu MaxMind được biên dịch trước. Mô-đun này không được xây dựng theo mặc định.

` --with-http_dav_module `: Cho phép xây dựng mô-đun ngx_http_dav_module cung cấp tự động hóa quản lý tệp thông qua giao thức WebDAV. Mô-đun này không được xây dựng theo mặc định.
 
` --with-http_flv_module ` : Cho phép xây dựng mô-đun ngx_http_flv_module cung cấp hỗ trợ phía máy chủ giả cho các tệp Flash Video (FLV). Mô-đun này không được xây dựng theo mặc định.

` --with-http_mp4_module ` : Cho phép xây dựng mô-đun ngx_http_mp4_module cung cấp hỗ trợ phía máy chủ giả cho các tệp MP4. Mô-đun này không được xây dựng theo mặc định.

` --with-http_gunzip_module ` : Cho phép xây dựng mô-đun ngx_http_gunzip_module giải nén các phản hồi với Mã hóa nội dung mã hóa: gzip, cho các máy khách không hỗ trợ phương thức mã hóa của gzip. Mô-đun này không được xây dựng theo mặc định.

` --with-http_gzip_static_module ` : Cho phép xây dựng mô-đun ngx_http_gzip_static_module cho phép gửi các tệp được nén bằng phần mở rộng tên tệp của .gz. Thay vì các tệp thông thường. Mô-đun này không được xây dựng theo mặc định.

` --with-http_auth_request_module ` : Cho phép xây dựng mô-đun ngx_http_auth_Vquest_module thực hiện ủy quyền của khách hàng dựa trên kết quả của một yêu cầu con. Mô-đun này không được xây dựng theo mặc định.

` --with-http_random_index_module ` : Cho phép xây dựng mô đun ngx_http_random_index_module xử lý các yêu cầu kết thúc bằng ký tự gạch chéo (’/,) và chọn một tệp ngẫu nhiên trong một thư mục để phục vụ như một tệp chỉ mục. Mô-đun này không được xây dựng theo mặc định.

` --with-http_secure_link_module ` : Cho phép xây dựng mô-đun ngx_http_secure_link_module. Mô-đun này không được xây dựng theo mặc định.

` --with-http_degradation_module ` : Cho phép xây dựng mô-đun ngx_http_degradation_module. Mô-đun này không được xây dựng theo mặc định.

` --with-http_slice_module ` : Cho phép xây dựng mô-đun ngx_http_slice_module phân chia yêu cầu thành các yêu cầu con, mỗi yêu cầu trả về một phạm vi phản hồi nhất định. Các mô-đun cungcấp bộ nhớ đệm hiệu quả hơn của các phản ứng lớn. Mô-đun này không được xây dựng theo mặc định.

` --with-http_stub_status_module ` : Cho phép xây dựng mô-đun ngx_http_stub_status_module cung cấp quyền truy cập vào thông tin trạng thái cơ bản. Mô-đun này không được xây dựng theo mặc định.

` --without-http_charset_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_charset_module để thêm bộ ký tự được chỉ định vào trường tiêu đề phản hồi Kiểu nội dung của Kiểu và có thể chuyển đổi dữ liệu từ bộ ký tự này sang bộ ký tự khác.

` --without-http_gzip_module ` : Vô hiệu hóa việc xây dựng một mô-đun nén các phản hồi của máy chủ HTTP. Thư viện zlib là cần thiết để xây dựng và chạy mô-đun này.

` --without-http_ssi_module ` : Không cho phép xây dựng mô-đun ngx_http_ssi_module xử lý các lệnh SSI (Bao gồm phía máy chủ) trong các phản hồi đi qua nó.

` --without-http_userid_module ` : Không cho phép xây dựng mô-đun ngx_http_userid_module để đặt cookie phù hợp với nhận dạng máy khách.

` --without-http_access_module ` : Không cho phép xây dựng mô-đun ngx_http_access_module cho phép giới hạn quyền truy cập vào một số địa chỉ máy khách nhất định.

` --without-http_auth_basic_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_auth_basic_module cho phép giới hạn quyền truy cập vào tài nguyên bằng cách xác thực tên người dùng và mật khẩu bằng giao thức xác thực cơ bản HTTP HTTP.

` --without-http_mirror_module ` : Không cho phép xây dựng mô-đun ngx_http_mirror_module thực hiện phản chiếu yêu cầu ban đầu bằng cách tạo các yêu cầu phản chiếu nền.

` --without-http_autoindex_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_autoindex_module xử lý các yêu cầu kết thúc bằng ký tự gạch chéo (’/,) và tạo danh sách thư mục trong trường hợp mô-đun ngx_http_index_module không thể tìm thấy tệp chỉ mục.

` --without-http_geo_module ` : Không cho phép xây dựng mô-đun ngx_http_geo_module tạo các biến có giá trị tùy thuộc vào địa chỉ IP của máy khách.

` --without-http_map_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_map_module tạo các biến có giá trị tùy thuộc vào giá trị của các biến khác.

` --without-http_split_clients_module ` : Không cho phép xây dựng mô-đun ngx_http_split_clents_module tạo các biến để thử nghiệm A / B.

` --without-http_referer_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_Vferer_module có thể chặn quyền truy cập vào một trang web đối với các yêu cầu có giá trị không hợp lệ trong trường tiêu đề của Tham chiếu giới thiệu.

` --without-http_rewrite_module ` : Vô hiệu hóa việc xây dựng một mô-đun cho phép máy chủ HTTP chuyển hướng các yêu cầu và thay đổi URI của các yêu cầu. Thư viện PCRE là cần thiết để xây dựng và chạy mô-đun này.

` --without-http_proxy_module ` : Vô hiệu hóa việc xây dựng một mô-đun ủy quyền máy chủ HTTP.

` --without-http_fastcgi_module ` : Không cho phép xây dựng mô-đun ngx_http_fastcgi_module chuyển yêu cầu đến máy chủ FastCGI.

` --without-http_uwsgi_module ` : Không cho phép xây dựng mô-đun ngx_http_uwsgi_module chuyển yêu cầu đến máy chủ uwsgi.

` --without-http_scgi_module ` : Không cho phép xây dựng mô-đun ngx_http_scgi_module chuyển yêu cầu đến máy chủ SCGI.

` --without-http_grpc_module ` : Không cho phép xây dựng mô-đun ngx_http_grpc_module chuyển yêu cầu đến máy chủ gRPC.

` --without-http_memcached_module ` : Không cho phép xây dựng mô-đun ngx_http_memcached_module để nhận phản hồi từ máy chủ memcached.

` --without-http_limit_conn_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_limit_conn_module giới hạn số lượng kết nối trên mỗi khóa, ví dụ: số lượng kết nối từ một địa chỉ IP duy nhất.

` --without-http_limit_req_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_limit_Vq_module giới hạn tốc độ xử lý yêu cầu trên mỗi khóa, ví dụ: tốc độ xử lý các yêu cầu đến từ một địa chỉ IP duy nhất.

` --without-http_empty_gif_module ` : Vô hiệu hóa việc xây dựng một mô-đun phát ra GIF trong suốt một pixel.

` --without-http_browser_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_http_browser_module để tạo các biến có giá trị phụ thuộc vào giá trị của trường tiêu đề yêu cầu của tác nhân người dùng-tác nhân.

` --without-http_upstream_hash_module ` : Vô hiệu hóa việc xây dựng một mô-đun thực hiện phương pháp cân bằng tải băm.

` --without-http_upstream_ip_hash_module ` : Vô hiệu hóa việc xây dựng một mô-đun thực hiện phương pháp cân bằng tải ip_hash.

` --without-http_upstream_least_conn_module ` : Vô hiệu hóa việc xây dựng một mô-đun thực hiện phương pháp cân bằng tải tối thiểu.

` --without-http_upstream_keepalive_module ` : Vô hiệu hóa việc xây dựng một mô-đun cung cấp bộ nhớ đệm của các kết nối đến các máy chủ ngược dòng.

` --without-http_upstream_zone_module ` : Vô hiệu hóa việc xây dựng một mô-đun cho phép lưu trữ trạng thái thời gian chạy của một nhóm ngược dòng trong vùng nhớ chung

`  --with-http_perl_module && --with-http_perl_module=dynamic ` : Cho phép xây dựng mô-đun Perl nhúng. Mô-đun này không được xây dựng theo mặc định.

` --with-perl_modules_path=path ` : Định nghĩa một thư mục sẽ giữ các mô-đun Perl.

` --with-perl=path ` : đặt tên của nhị phân Perl.

` --http-log-path=path ` : Đặt tên của tệp nhật ký yêu cầu chính của máy chủ HTTP. Sau khi cài đặt, tên tệp luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh access_log. Theo mặc định, tệp được đặt tên là tiền tố / log / access.log.

` --http-client-body-temp-path=path ` : Định nghĩa một thư mục để lưu trữ các tệp tạm thời chứa các thân yêu cầu của máy khách. Sau khi cài đặt, thư mục luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh client_body_temp_path. Theo mặc định, thư mục được đặt tên là tiền tố / client_body_temp.

` --http-proxy-temp-path=path ` : Định nghĩa một thư mục để lưu trữ các tệp tạm thời với dữ liệu nhận được từ các máy chủ proxy. Sau khi cài đặt, thư mục luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh proxy_temp_path. Theo mặc định, thư mục được đặt tên là tiền tố / proxy_temp.

` --http-fastcgi-temp-path=path ` : Định nghĩa một thư mục để lưu trữ các tệp tạm thời với dữ liệu nhận được từ các máy chủ FastCGI. Sau khi cài đặt, thư mục luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh fastcgi_temp_path. Theo mặc định, thư mục được đặt tên là tiền tố / fastcgi_temp.

` --http-uwsgi-temp-path=path ` : Định nghĩa một thư mục để lưu trữ các tệp tạm thời với dữ liệu nhận được từ các máy chủ uwsgi. Sau khi cài đặt, thư mục luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh uwsgi_temp_path. Theo mặc định, thư mục được đặt tên là tiền tố / uwsgi_temp

` --http-scgi-temp-path=path ` : Định nghĩa một thư mục để lưu trữ các tệp tạm thời với dữ liệu nhận được từ các máy chủ SCGI. Sau khi cài đặt, thư mục luôn có thể được thay đổi trong tệp cấu hình nginx.conf bằng cách sử dụng lệnh scgi_temp_path. Theo mặc định, thư mục được đặt tên là tiền tố / scgi_temp.

` --without-http ` : Vô hiệu hóa máy chủ HTTP

` --without-http-cache `: Vô hiệu hóa bộ đệm HTTP

` --with-mail && --with-mail=dynamic ` : Cho phép máy chủ proxy thư POP3 / IMAP4 / SMTP.

` --with-mail_ssl_module ` : Cho phép xây dựng một mô-đun bổ sung hỗ trợ giao thức SSL / TLS cho máy chủ proxy thư. Mô-đun này không được xây dựng theo mặc định. Thư viện OpenSSL là cần thiết để xây dựng và chạy mô-đun này.

` --without-mail_pop3_module ` : Vô hiệu hóa giao thức POP3 trong máy chủ proxy mail.

` --without-mail_imap_module ` : Vô hiệu hóa giao thức IMAP trong máy chủ proxy mail.

` --without-mail_smtp_module ` : Vô hiệu hóa giao thức SMTP trong máy chủ proxy mail.

` --with-stream && --with-stream=dynamic ` : Cho phép xây dựng mô-đun truyền phát để ủy quyền TCP / UDP chung và cân bằng tải. Mô-đun này không được xây dựng theo mặc định.

` --with-stream_ssl_module ` : Cho phép xây dựng một mô-đun bổ sung hỗ trợ giao thức SSL / TLS cho mô-đun truyền phát. Mô-đun này không được xây dựng theo mặc định. Thư viện OpenSSL là cần thiết để xây dựng và chạy mô-đun này.

` --with-stream_realip_module ` : Cho phép xây dựng mô đun ngx_stream_realip_module thay đổi địa chỉ máy khách thành địa chỉ được gửi trong tiêu đề giao thức PROXY. Mô-đun này không được xây dựng theo mặc định.

` --with-stream_geoip_module && --with-stream_geoip_module=dynamic ` : Cho phép xây dựng mô đun ngx_stream_geoip_module tạo các biến tùy thuộc vào địa chỉ IP của máy khách và cơ sở dữ liệu MaxMind được biên dịch trước. Mô-đun này không được xây dựng theo mặc định.

` --with-stream_ssl_preread_module ` : Cho phép xây dựng mô-đun ngx_stream_ssl_preread_module cho phép trích xuất thông tin từ tin nhắn ClientHello mà không cần chấm dứt SSL / TLS. Mô-đun này không được xây dựng theo mặc định.

` --without-stream_limit_conn_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_stream_limit_conn_module giới hạn số lượng kết nối trên mỗi khóa, ví dụ: số lượng kết nối từ một địa chỉ IP duy nhất.

` --without-stream_access_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_stream_core_module cho phép giới hạn quyền truy cập vào một số địa chỉ khách hàng nhất định.

` --without-stream_geo_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_stream_core_module tạo các biến có giá trị tùy thuộc vào địa chỉ IP của máy khách.

` --without-stream_map_module ` : Vô hiệu hóa việc xây dựng mô đun ngx_stream_core_module tạo các biến có giá trị tùy thuộc vào giá trị của các biến khác.

` --without-stream_split_clients_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_stream split_clents tạo các biến để thử nghiệm A / B.

` --without-stream_return_module ` : Vô hiệu hóa việc xây dựng mô-đun ngx_stream_core_module gửi một số giá trị cụ thể đến máy khách và sau đó đóng kết nối.

` --without-stream_upstream_hash_module `: Vô hiệu hóa việc xây dựng một mô-đun thực hiện phương pháp cân bằng tải băm.

` --without-stream_upstream_least_conn_module ` : Vô hiệu hóa việc xây dựng một mô-đun thực hiện phương pháp cân bằng tải tối thiểu.

` --without-stream_upstream_zone_module ` : Vô hiệu hóa việc xây dựng một mô-đun cho phép lưu trữ trạng thái thời gian chạy của một nhóm ngược dòng trong vùng nhớ chung.

` --with-google_perftools_module ` : Cho phép xây dựng mô-đun ngx_google_perftools_module cho phép định hình các quy trình nhân viên nginx bằng Google Performance Tools. Mô-đun dành cho các nhà phát triển nginx và không được xây dựng theo mặc định.

` --with-cpp_test_module` : Cho phép xây dựng mô-đun ngx_cpp_test_module.

` --add-module=path ` : Cho phép thêm một mô-đun bên ngoài.

` --add-dynamic-module=path` : Cho phép một mô-đun động bên ngoài.

` --with-compat ` : Cho phép tương thích mô-đun động.

` --with-cc=path ` : Đặt tên của trình biên dịch C.

` --with-cpp=path ` : Đặt tên của bộ tiền xử lý C.

` --with-cc-opt=parameters ` : Đặt các tham số bổ sung sẽ được thêm vào biến CFLAGS. Khi sử dụng thư viện PCRE hệ thống trong FreeBSD, nên chỉ định --with-cc-opt = "- I / usr / local / include". Nếu số lượng tệp được hỗ trợ bởi select () cần tăng lên, nó cũng có thể được chỉ định ở đây như sau: --with-cc-opt = "- D FD_SETSIZE = 2048".

` --with-ld-opt=parameters ` : Thiết lập các tham số bổ sung sẽ được sử dụng trong quá trình liên kết. Khi sử dụng thư viện PCRE hệ thống trong FreeBSD, --with-ld-opt = "- L / usr / local / lib" phải được chỉ định.

` --with-cpu-opt=cpu ` : Cho phép xây dựng trên mỗi CPU được chỉ định: pentium, pentiumpro, pentium3, pentium4, athlon, opteron, sparc32, sparc64, ppc64.

` --without-pcre` : Vô hiệu hóa việc sử dụng thư viện PCRE.

` --with-pcre ` : Buộc sử dụng thư viện PCRE.

` --with-pcre=path ` : Đặt đường dẫn đến các nguồn của thư viện PCRE. Phân phối thư viện (phiên bản 4.4 - 8.43) cần được tải xuống từ trang PCRE và trích xuất. Phần còn lại được thực hiện bởi nginx từ ./mình và thực hiện. Thư viện là cần thiết để hỗ trợ các biểu thức chính quy trong chỉ thị vị trí và cho mô-đun ngx_http_rewrite_module.

` --with-pcre-opt=parameters ` : Thiết lập các tùy chọn xây dựng bổ sung cho PCRE.

` --with-pcre-jit `: Xây dựng thư viện PCRE với chương trình biên dịch đúng thời gian của Hỗ trợ (1.1.12, chỉ thị pcre_jit).

` --with-zlib=path ` : đặt đường dẫn đến các nguồn của thư viện zlib. Phân phối thư viện (phiên bản 1.1.3 - 1.2.11) cần được tải xuống từ trang zlib và trích xuất. Phần còn lại được thực hiện bởi nginx từ ./mình và thực hiện. Thư viện là cần thiết cho mô-đun ngx_http_gzip_module.

` --with-zlib-opt=parameters ` : Thiết lập các tùy chọn xây dựng bổ sung cho zlib.

` --with-zlib-asm=cpu ` : Cho phép sử dụng các nguồn trình biên dịch mã zlib được tối ưu hóa cho một trong các CPU được chỉ định: pentium, pentiumpro.

` --with-libatomic ` : Buộc sử dụng thư viện libatomic_ops.

` --with-libatomic=path ` : Đặt đường dẫn đến các nguồn thư viện libatomic_ops.

` --with-openssl=path ` : Đặt đường dẫn đến các nguồn thư viện OpenSSL.

` --with-openssl-opt=parameters ` : Đặt các tùy chọn xây dựng bổ sung cho OpenSSL.

` --with-debug ` : Cho phép nhật ký gỡ lỗi.

##### Ví dụ : 
```
./configure
    --sbin-path=/usr/local/nginx/nginx
    --conf-path=/usr/local/nginx/nginx.conf
    --pid-path=/usr/local/nginx/nginx.pid
    --with-http_ssl_module
    --with-pcre=../pcre-8.43
    --with-zlib=../zlib-1.2.11

```







