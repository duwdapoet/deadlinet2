#### 1. HTTP Protocol:
- HTTP (HyperText Transfer Protocol - Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW.
- HTTP là một giao thức ứng dụng của bộ giao thức TCP/IP (các giao thức nền tảng cho Internet).
- Giao thức này hoạt động dựa trên mô hình Client – Server. Trong mô hình này, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.
- HTTP là một stateless protocol. Hay nói cách khác, request hiện tại không biết những gì đã hoàn thành trong request trước đó.
- HTTP cho phép tạo các yêu cầu gửi và nhận các kiểu dữ liệu, do đó cho phép xây dựng hệ thống độc lập với dữ liệu được truyển giao.

#### 2. HTTP Requests là gì?
- HTTP request là thông tin được gửi từ client lên server, để yêu cầu server tìm hoặc xử lý một số thông tin, dữ liệu mà client muốn. HTTP request có thể là một file text dưới dạng XML hoặc Json mà cả hai đều có thể hiểu được.

#### 3. HTTP Responses:
- HTTP Responses là một thông điệp trả lại từ máy chủ web cho trình duyệt của người dùng sau khi nhận được một yêu cầu từ trình duyệt. Phản hồi này bao gồm một mã trạng thái HTTP và một nội dung phản hồi.
- Ví dụ: khi ta nhập vào địa chỉ google.com, kết quả mà server trả về cho ta sẽ là giao diện của website và các thông tin của header. Gồm những đoạn mã HTML kèm theo các thông tin của header. Browser sẽ dựa vào các thông tin này để hiển thị trạng thái kết quả của request. Mã HTML dùng để hiển thị giao diện của website. Nếu ta nhập vào một địa chỉ không tồn tại thì thông tin của header cũng sẽ không có gì.

#### 4. HTTP Methods:
- Có tất cả 9 phương thức gồm: GET, HEAD, POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE. Trong đó GET và POST là hai phương thức thông dụng nhất.

Phương thức GET:
- GET là phương thức được Client gửi dữ liệu lên Server thông qua đường dẫn URL nằm trên thanh địa chỉ của Browser. Server sẽ nhận đường dẫn đó và phân tích trả về kết quả cho bạn. Hơn nữa, nó là một phương thức được sử dụng phổ biến mà không cần có request body.
- Ví dụ điển hình là khi bạn mở một trang web, Client sẽ gửi một phương thức Get lên server để truy xuất nội dung hiển thị của trang web. Nó tương đương với thao tác đọc.

Một số đặc điểm chính của phương thức GET:
- Giới hạn độ dài của các giá trị là 255 kí tự.
- Chỉ hỗ trợ các dữ liệu kiểu String.
- Có thể lưu vào bộ nhớ cache.
- Các tham số truyền vào được lưu trữ trong lịch sử trình duyệt.
- Có thể được bookmark (đánh dấu rồi xem lại sau) do được lưu trong lịch sử trình duyệt.

Phương thức POST:
- POST là phương thức gửi dữ liệu đến server giúp bạn có thể thêm mới dữ liệu hoặc cập nhật dữ liệu đã có vào database.
- Chúng ta sẽ gửi thông tin cần thêm hoặc cập nhật trong phần body request.

Một số đặc điểm chính của Post là:
- Dữ liệu cần thêm hoặc cập nhật không được hiển thị trong URL của trình duyệt.
- Dữ liệu không được lưu trong lịch sử trình duyệt.
- Không có hạn chế về độ dài của dữ liệu.
- Hỗ trợ nhiều kiểu dữ liệu như: String, binary, integers,..

Phương thức HEAD: phương thức này gần giống với GET, tuy nhiên nó không có response body.

Phương thức PUT: Cách hoạt động tương tự như Post nhưng nó chỉ được sử dụng để cập nhật dữ liệu đã có trong database. Khi sử dụng nó, bạn phải sửa toàn bộ dữ liệu của một đối tượng.

Phương thức PATCH: Tượng tự như Post và Put, nhưng Patch được sử dụng khi phải cập nhật một phần dữ liệu của đối tượng.

Phương thức DELETE: Giống như tên gọi, khi sử dụng phương thức Delete sẽ xoá các dữ liệu của server về tài nguyên thông qua URI. Cũng giống như GET, phương thức này không có body request.

Phương thức CONNECT: thiết lập một kết nối tới server theo URI.

Phương thức OPTIONS: mô tả các tùy chọn giao tiếp cho resource.

Phương thức TRACE: thực hiện một bài test loop - back theo đường dẫn đến resource.

#### 5. URLs:
Khái niệm: URL là viết tắt của Uniform Resource Locator, được sử dụng để xác định địa chỉ của một tài nguyên trên Internet.

URL bao gồm các thành phần sau:
- Scheme (giao thức): Là phần đầu tiên của URL, chỉ định giao thức được sử dụng để truy cập tài nguyên, ví dụ như HTTP, HTTPS, FTP, SMTP, và telnet.
- Host (máy chủ): Là phần tiếp theo của URL, chỉ định tên miền hoặc địa chỉ IP của máy chủ mà tài nguyên được lưu trữ trên đó.
- Port (cổng): Là phần tiếp theo của URL, chỉ định cổng mà máy chủ sử dụng để chấp nhận kết nối từ các yêu cầu.
- Path (đường dẫn): Là phần tiếp theo của URL, chỉ định đường dẫn đến tài nguyên trên máy chủ.
- Query string (chuỗi truy vấn): Là phần tiếp theo của URL, chứa các tham số và giá trị được truyền cho máy chủ để xử lý.
- Fragment (đoạn): Là phần cuối cùng của URL, chỉ định một phần của tài nguyên cụ thể để hiển thị cho người dùng, ví dụ như một vị trí trên trang web hoặc một điểm thời gian trong video.

#### 6. HTTP Headers:
