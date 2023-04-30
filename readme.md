#### 1. HTTP Protocol:
- HTTP (HyperText Transfer Protocol - Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW.
- HTTP là một giao thức ứng dụng của bộ giao thức TCP/IP (các giao thức nền tảng cho Internet).
- Giao thức này hoạt động dựa trên mô hình Client – Server. Trong mô hình này, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.
- HTTP là một stateless protocol. Hay nói cách khác, request hiện tại không biết những gì đã hoàn thành trong request trước đó.
- HTTP cho phép tạo các yêu cầu gửi và nhận các kiểu dữ liệu, do đó cho phép xây dựng hệ thống độc lập với dữ liệu được truyển giao.

#### 2. HTTP Requests là gì?
- HTTP request là thông tin được gửi từ client lên server, để yêu cầu server tìm hoặc xử lý một số thông tin, dữ liệu mà client muốn. HTTP request có thể là một file text dưới dạng XML hoặc Json mà cả hai đều có thể hiểu được.
- Cấu trúc của HTTP request: Request line và Body request ( có thể có hoặc không).
- Request line là dòng đầu tiên trong HTTP request. Nó bao gồm 3 phần: phương thức HTTP được sử dụng, URI( Uniform Resource Identifier) giúp xác định các tài nguyên mà client yêu cầu, phiên bản của giao thức HTTP.

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
- HTTP Header là một phần của HTTP và truyền thông tin bổ sung trong các request hoặc phản hồi HTTP. Thông qua server web của trang web được gọi mà dữ liệu được gửi tới trình duyệt, thông qua HTTP Header mà server và trình duyệt trao đổi thông tin meta về tài liệu.

Request Headers:

Request header giúp client có thể gửi yêu cầu lên server. Mỗi yêu cầu sẽ kèm theo các thông số, và các thông số đó được gọi là Header Parameters.

Trình duyệt và server sẽ dựa vào các thông số header này để trả dữ liệu và hiển thị dữ liệu cho phù hợp, các thông số mà chúng ta thường xuyên gặp:
- User-Agent: cho phép server xác định ứng dụng, hệ điều hành, nhà cung cấp và phiên bản.
- Connection: kiểm soát kết nối mạng. Nói cách khác, cho phép dừng hoặc tiếp tục kết nối sau khi server thực hiện xong yêu cầu.
- Cache-Control: chỉ định chính sách bộ nhớ đệm của trình duyệt.
- Accept-Language: cho biết tất cả các ngôn ngữ (tự nhiên) mà client có thể hiểu được.
- Host: xác định tên miền hoặc địa chỉ IP của máy chủ web mà yêu cầu được gửi đến.
- Authorization: chứa thông tin xác thực người dùng (username và password) để truy cập vào các trang web bảo mật.
- Cookie: Trường này chứa các cookie được gửi đến từ trình duyệt của người dùng. Cookie được sử dụng để lưu trữ thông tin về người dùng và các thông tin khác như thông tin giỏ hàng, lịch sử truy cập, v.v.
- Referer: chỉ ra địa chỉ URL của trang web mà yêu cầu được gửi từ đó

Respond Headers:

Response Header là các thông tin được gửi từ máy chủ web đến trình duyệt của người dùng như phản hồi cho một yêu cầu HTTP Request. Header này chứa các thông tin về nội dung trả về, thông tin về máy chủ, thông tin về mã trạng thái và các thông tin khác liên quan đến phản hồi.

Các trường header thông thường bao gồm:
- Date: Chứa thời gian máy chủ phản hồi yêu cầu.
- erver: Chứa thông tin về mã và phiên bản của máy chủ web.

- Content-Type: Chứa thông tin về định dạng của nội dung trả về (ví dụ: text/html).

- Content-Length: Chứa thông tin về kích thước của nội dung trả về.

- Cache-Control: Chứa các chỉ thị về bộ nhớ đệm cho các trình duyệt để giảm tải tài nguyên của máy chủ.

- Expires: Chứa thời gian hết hạn của nội dung được lưu trữ trong bộ nhớ đệm của trình duyệt.

- Location: Chứa địa chỉ URL mới nếu phản hồi là một chuyển hướng (redirect).

- Set-Cookie: Chứa các thông tin về cookie được thiết lập cho trình duyệt.

- Content-Encoding: Chứa thông tin về phương thức nén được sử dụng cho nội dung trả về.

#### 7. Cookies:
Cookies là một tập hợp các tệp thông tin do chính người dùng tạo ra mỗi lần truy cập vào một website nào đó và để lại dữ liệu duyệt web. Thông tin Cookie sẽ thường được lưu dưới dạng cặp tên name – value.

Các đoạn mã Cookie sẽ giúp tối ưu trải nghiệm người dùng nhờ khả năng lưu trữ thông tin và đề xuất nội dung phù hợp cho các lần truy cập tiếp theo. Thông thường, chúng sẽ ghi nhớ trạng thái đăng nhập, tùy chọn trang, các bộ lọc liên quan,… của người dùng.

Cookies được phân làm 2 loại chính đó là Session cookies (phiên cookies) và Persistent cookies (coookies liên tục).
- Session cookies (phiên cookies): cookies này được giữ lại ở trình duyệt và sẽ bị xóa bỏ khi đóng trình duyệt. Khi cửa sổ trình duyệt mới được mở lại, người dùng sẽ phải cung cấp lại các chứng thực của mình.
- Persistent cookies (coookies liên tục): cookies này được giữ ở trình duyệt cho tới khi hết hạn hoặc được xóa một cách thủ công. Các trang web sẽ ghi nhớ các chứng thực ngay cả khi người dùng đóng trình duyệt.

Ngoài ra còn có Cookies bên thứ ba, cookies này có chức năng tìm kiếm dữ liệu liên quan tới hoạt động online của bạn để gửi cho chủ sở hữu web đang muốn cải thiện quảng cáo.

Cách thức hoạt động của Cookies:
- Khi người dùng truy cập vào trang web lần đầu tiên, trang web sẽ tạo ra bản ghi của nó và lưu vào cookies trên trình duyệt của người dùng. Lúc này cookies chỉ là một dòng văn bản ngắn, nó không chứa bất cứ thông tin nào về người dùng hoặc máy của người dùng. Thay vào đó, nó chứa URL của trang web đã đặt cookie.
- Khi người dùng quay lại và lướt web, mỗi trang mới mà người dùng truy cập, trình duyệt sẽ tìm kiếm cookies. Nếu URL của cookies khớp với URL của trang web, trang web sẽ truy xuất thông tin máy chủ bằng cách sử dụng thông tin lấy được từ cookies.
- Bằng cách này, trang web có thể nâng cao trải nghiệm người dùng, hạn chế phải lặp đi lặp lại nhiều hoạt động của người dùng. Một số trang web cũng có thể sử dụng cookies để nâng cao trải nghiệm người dùng, người dùng mới có thể thấy phiên bản mới của trang web, trong khi người dùng cũ lại thấy phiên bản trước đó.

Cookies bao gồm:
- Name: Một tên duy nhất dùng để định danh, tên cookies không phân biệt chữ hoa chữ thường và nó phải được mã hóa URL.
- Value: giá trị được lưu trữ trong cookies, giá trị này cũng nên được mã hóa URL.
- Domain: là domain mà cookies chúng ta hợp lệ, mọi thứ được gửi hoặc được sử dụng từ domain này sẽ kèm theo cookies.
- Path: đường dẫn được chỉ định trong domain, nơi mà cookies sẽ được gửi đến server.
- Expiration: dấu thời gian, nó cho biết lúc nào cookies sẽ bị xóa. Mặc định thì tất cả cookies sẽ bị xóa khi ta tắt trình duyệt. Tuy nhiên, ta có thể xác định thời gian cố định để xóa, giá trị này được đặt theo định dạng GMT và sau thời gian được quy định, cookies sẽ bị xóa ngay lập tức.
- Secure Flag: cờ an toàn, với mục đích chỉ gửi cookies nếu kết nối SSL được sử dụng.
