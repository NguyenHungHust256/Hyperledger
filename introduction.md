<h4>Introduction</h4>
<p>Hyperledger Fabric là một platform của distributed ledger solutions được củng cố bởi một hệ thống mang lại sự an toàn trong bảo mật, khả năng phục hồi, tính linh hoạt và co giãn. Nó được thiết kế được cung cấp triển khai các thành phần khác nhau, phù hợp vơi sự phức tạp.</p>
<p>Hyperledger Fabric cung cấp một kiến ​​trúc đàn hồi và mở rộng độc đáo, phân biệt nó với các giải pháp blockchain thay thế. Lập kế hoạch xây dựng blockchain cho doanh nghiệp, mã nguồn mở. HLF là điểm khởi đầu của bạn.</p>
<h4>Hyperledger Fabric là gì?</h4>
<p>Linux Foundation thành lập Hyperledger vào năm 2015 để nâng cao công nghệ blockchain. Nó khuyến khích mọi người tham gia để phát triển công nghệ blockchain.</p>
<p>Hyperledger Fabric là một trong các dự án blockchain trong Hyperledger. Giống như các công nghệ blockchain khác, nó có 1 ledger, sử dụng smart contracts và là một hệ thống bởi người tham gia quản lý giao dịch của họ</p>
<p>Hyperledger Fabric khác với một vài hệ thống blockchain khác là nó là private và permissioned. Thay vì một hệ thống cấp phép mở cho phép các định danh không xác định tham gia vào mạng (yêu cầu các giao thức như Proof of Work để xác thực giao dịch và bảo mật mạng), các thành viên của mạng lưới Hyperledger Fabric đăng ký thông qua một Nhà cung cấp dịch vụ thành viên đáng tin cậy (MSP).</p>
<p>Hyperledger cũng cung cấp khả năng để tạo channels, cho phép một nhóm người tham gia tạo một sổ cái giao dịch riêng. Đây là một tuỳ  chọn đặc biệt của mạng, Nếu hai người tham gia tạo thành một kênh, thì những người tham gia đó - và không có người nào khác - có bản sao sổ cái của kênh đó. </p>
<h5>Shared Ledger</h5>
<p>Hyperledger Fabric là một hệ thống con sổ cái bao gồm 2 components: The World State và Transaction Log. Mỗi người tham gia có một bản sao của ledger </p>
<p>The world state component diễn tả một trạng thái của ledger ở 1 thời điểm nhất định. Nó là cơ sở dữ liệu của ledger. The transaction log component ghi lại tất cả transactions đã dẫn đến kết quả của wordld state, nó là lịch sử cập nhật của world state.  Sổ cái là sự kết hợp của world state database và lịch sử transaction log </p>
<p>Sổ cái có một kho lưu trữ dữ liệu cho world state. Theo mặc định, đây là một cơ sở dữ liệu LevelDB key-value. Transaction logs không cần thiết pluggable. Nó đơn giản ghi lại giá trị trước và sau của cơ sở dữ liệu của sổ kế toán đang được sử dụng bởi mạng blockchain.</p>
<h5>Smart Contracts</h5>
<p>Hyperledger Fabric smart contracts được viết trong <i>chaincode</i> và được gọi bởi một ứng dụng blockchain bên ngoài khi ứng dụng đó cần tương tác với sổ cái. Trong hầu hết các trường hợp, chaincode tương tác chỉ với thành phần cơ sở dữ liệu của sổ cái, the world state (ví dụ như truy vấn đến nó) và không có transaction log</p>
<p>Chaincode có thể được thực hiện trên một vài ngôn ngữ lập trình. Hiện tại ngôn ngữ hỗ trợ chaincode là Go với Java,...</p>
<h5>Privacy</h5>
<p>Trong một mạng, người tham gia trong Business-to-Business (B2B) network vô cùng nhạy cảm về bao nhiêu thông tin họ chia sẽ. Đối với các mạng khác, vấn đề riêng tư không phải là mối quan tâm hàng đầu.</p>
<p>Hyperledger Fabric hỗ trợ mạng nơi mà quền riêng tư là một yêu cầu hoạt động chính cũng như các mạng tương đối mở</p>
<h5>Consensus</h5>


