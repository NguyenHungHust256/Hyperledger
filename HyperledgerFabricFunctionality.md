<h1>Hyperledger Fabric Functionalities</h1>
<p>Hyperledger Fabric là một triển khai của công nghệ sổ cái phân tán (DLT) cung cấp tính bảo mật, co giãn, và hiệu suất, trong một kiến trúc blockchain của mạng công nghiệp</p>
<h5>Quản lý danh tính</h5>
<p>Để bật mạng cho phép, Hyperledger Fabric cung cấp một dịch vụ nhận dạng các thành viên, quản lý user IDs và xác thực tất cả người tham gia trên mạng. Danh sách kiểm soát truy cập có thể được dùng để cung cấp các lớp bổ sung cho phép thông qua uỷ quyền của các hoạt động mạng. Cho ví dụ, một user ID cụ thể có thể được phép gọi một ứng dụng chaincode, nhưng bị chặn triển khai new chaincode </p>
<h5>Quyền riêng tư và bảo mật</h5>
<p>Hyperledger Fabric cho phép cạnh tranh các lợi ích kinh tế và bất kỳ nhóm nào yêu cầu giao dịch bảo mật, riêng tư thì cùng tồn tại trên một mạng cho phép. Private Channels là các cái thông điệp bị hạn chế có thể được sử dụng để cung cấp quyền riêng tư và bảo mật giao dịch cho các thành viên của mạng con. Tất cả dữ liệu, bao gồm transaction, member và thông tin channel, trong một channel là không xuất hiện và không thể truy cập được đối với bất kỳ thành viên mạng nào không được cấp quyền truy cập rõ ràng vào kênh đó.</p>
<h5>Xử lý hiệu quả</h5>
<p>Hyperledger Fabric gán vai trò theo loại nút. Cho phép xử lý nhiều giao dịch đồng thời trên một node. Việc xử lý đồng thời làm tăng hiệu quả xử lý trên mỗi peer và đẩy nhanh việc phân phối các giao dịch</p>
<h5>Chaincode Functionality</h5>
<p>Chaincode application mã hoá logic được gọi bởi các loại transaction đặc biệt trong kênh. Chaincode xác định các thông số cho thay đổi quyền sở hữu nội dung, đảm bảo rằng tất cả các giao dịch chuyển quyền sở hữu đều tuân theo các quy tắc và yêu cầu tương tự. System chaincode được xác định như một chaincode các định các tham số vận hành cho toàn bộ kênh. Vòng đời hệ thống và cấu hình chuỗi mã xác định các quy tắc cho kênh.</p>
<h5>Thiết kế mô đun</h5>
<p>Hyperledger Fabric thực hiện một kiến trúc môdun để cung cấp sự lựa chọn chức năng cho các nhà thiết kế mạng. Thuật toán đặc biệt để xác định, đồng thuận và mã hoá. Kết quả là một kiến ​​trúc blockchain phổ quát mà bất kỳ ngành công nghiệp có thể áp dụng, với sự đảm bảo rằng các mạng của nó sẽ tương thích với nhau trên thị trường, các ranh giới theo quy định và địa lý.</p>
