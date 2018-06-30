# Identify
<h4>Identify là gì?</h4>
<p>Các nhân tố khác nhau trong một mạng blockchain bao gồm các peer, orderers, client application, administrators,... Mỗi nhân tố - phần tử hoạt động trong hoặc ngoài một mạng có khả năng dùng dịch vụ. Những danh tính này thực sự quan trọng bởi vì chúng quyết định các quyền chính xác đối với tài nguyên và truy cập thông tin mà các tác nhân có trong một mạng blockchain</p>
<p> Có thêm một vài thuộc tính mà Fabric sử dụng để xác định quyền và nó cung cấp một principal. Principal giống như userIDs hoặc groupIDs, nhưng  linh hoạt hơn một chút bởi vì chúng có thể bao gồm một loạt thuộc tính của một định danh nhân tố, chẳng hạn như actor's organization, organization unit, vai trò hoặc thậm trí định danh đặc biệt của actor. Khi chúng ta nói về principals, chúng là các thuộc tính quyết định quyền của họ.</p>
<p>Để danh tính được xác thực, nó phải đến từ một cơ quan thẩm quyền đáng tin cậy. Nhà điều hành dịch vụ thành viên (membership service provider) (MSP)  là cách đạt được điều này trong Fabric. Đặc biệt hơn, một MSP là một thành phần định nghĩa luật chi phối các thông tin nhận dạng hợp lệ cho tổ chức này.  MSP mặc định triển khai trong fabric sử dụng chứng chỉ X.509 làm danh tính, chấp nhận một Public Key Infrastructure truyền thống (PKI)  mô hình phân cấp </p>
<h5>Một kịch bản đơn giản để giải thích cách sử dụng một danh tính</h5>
<p>Tưởng tượng rặng bạn thăm một siêu thị để mua một vài cửa hàng tạp hoá. Khi thanh toán bạn thấy một kí hiệu nói rằng chỉ có visa, mastercard, và AMEX card được chấp nhận. Nếu bạn cố gắng trả với thẻ khác, hay còn gọi là một "ImagineCard"- nó không  quan trọng liệu thẻ có xác thực hay không và bạn có đủ tiền trong tài khoản của mình. Nó sẽ không chấp nhận</p>
<img src="http://sv1.upsieutoc.com/2018/06/28/Screenshot-from-2018-06-28-16-06-59.png" />
<a>Có một thẻ tín dụng hợp lệ là không đủ - nó cũng phải được chấp nhận bởi các cửa hàng! PKIs và MSPs làm việc cùng nhau theo cách tương tự- một PKI cung cấp một danh sách các danh tính, và một MSP cho biết đó là thành viên của một tổ chức cụ thể tham gia vào mạng</a>
<p>Cơ quan cấp chứng chỉ PKI và MSPs cung cấp một sự kết hợp tương tự của các chức năng. Một PKI giống như một nhà cung cấp thẻ - nó cho biết nhiều loại danh tính xác thực khác nhau. Một MSP, theo một cách khác, nó giống như danh sách các thẻ cung cấp được chấp nhận bởi cửa hàng, xác định thành viên nào là thành viên đáng tin cậy của mạng thanh toán tại cửa hàng. MSPs ác thực danh tính các thành viên của mạng blockchain.</p>
<p>Hãy xem xét kỹ các khái niệm này chi tiết hơn một chút</p>
<h5>PKIs là gì?</h5>
<p>Một public key infrastructure (PKI) là một bộ sưu tập các công nghệ internet cung cấp thông tin liên lạc an toàn trong mạng. Nó là PKI mà đặt S trong HTTPS - và nếu bạn đang đọc tài liệu này trên mạng web browser, bạn có lẽ sử dụng PKI để đảm bảo rằng nó đến từ một nguồn xác thực</p>
<img src="http://sv1.upsieutoc.com/2018/06/28/Screenshot-from-2018-06-28-16-57-02.png" />
<a>Các thành phần của Public Key Infrastructure (PKI). Một PKI bao gồm Certificate Authorities, người cấp chứng chỉ kỹ thuật cho các bên (ví dụ: users of a service, service provider),người sau đó sử dụng chúng để xác thực mình trong các thông điệp trao đổi với môi trường của họ. Một danh sách  thu hồi chứng chỉ (CA's Certificate Revocation List (CRL)) tạo thành một tham chiếu cho các chứng chỉ không còn giá trị. Việc thu hôi chứng chỉ có thể xảy ra vì một số lý do. Ví dụ, một chứng chỉ có thể bị thu hồi bởi vì tài liệu riêng tư mật mã liên quan đến chứng chỉ đã được trưng ra.</a>
<p>Mặc dù, một mạng blockchain network không chỉ là một mạng lưới liên lạc, nó phụ thuộc vào chuẩn PKI để đảm bảo bảo mật giao tiếp giữa những người tham gia mạng khác nhau và đảm bảo rằng thông điệp trong blockchain là được xác định chính xác. Vì thế nó là quan trọng để hiểu cơ bản của PKI và lý do MSPs là rất quan trọng.</p>
<p>Có 4 thành phần chính của PKI:</p>
<li>Digital Certificates</li>
<li>Public and Private keys</li>
<li>Certificate Authorities</li>
<li>Certificate Revocation Lists</li>
<h5>Digital Certificates</h5>
<p>Một digital Certificate là một document giữ một tập hợp các thuộc tính liên quan tới chủ sỡ hữu chứng chỉ. Đa số các loại chứng chỉ là tuân thủ chuẩn X.509, cái mà cho phép mã hoá xác định chi tiết tổ chức trong cấu trúc đó.</p>
<p> Ví dụ, Mary Morris trong Manufacturing Division của Mitchell Cars trong Detroit, Michigan phải có một chứng chỉ số với một thuộc tính SUBJECT của C =US, `ST=Michigan`, `L=Detroit`, `O=Mitchell  Cars`, `OU=Manufacturing`, `CN=Mary  Morris  /UID=123456`. Trong cái digital certificate thì Public key được điền vào, còn private key thì không. </p>
<p>Không thể gỉả mạo chứng chỉ kỹ thuật số</p>
<h5>Authentication, Public Key và Private key</h5>
<p>Xác thực và thư toàn vẹn à một khái niệm quan trọng trong bảo mật giao tiếp. Xác thực yêu cầu. Xác thực yêu cầu các bên trao đổi tin nhắn được đảm bảo về danh tính đã tạo ra một thông điệp cụ thể</p>
<p>Cơ chế xác nhận truyền thống dựa vào digital signatures, như cái tên của nó, nó cho phép một bên ký thư điện tử của mình. Digital signatures cũng cung cấp đảm bảo về tính toàn vẹn của tin nhắn đã kí.</p>
<p>Về mặt kỹ thuật, cơ chế chữ ký số yêu cầu mỗi bên giữ 2 khoá mật mã: một public key được sử dụng rộng rãi và hoạt động như neo xác thực, và một private key được sử dụng để tạo chữ ký số trong thông điệp. Người nhận của chữ ký thông điệp có thể xác thực nguồn gốc và tính toàn vẹn của thông điệp nhận bởi kiểm tra chữ ký đính kèm có giá trị theo khoá công khai của người gửi dự kiến.  </p>
<p>Mối quan hệ độc đáo giữa khóa riêng tư và khóa công khai tương ứng là ma thuật mã hóa giúp truyền thông an toàn có thể. Mối quan hệ toán học duy nhất giữa các khoá là khoá riêng tư có thể được sử dụng để tạo chữ ký trên một thông điệp mà chỉ có khoá công khai tương ứng mới chỉ có thể khớp và trên cùng thông điệp. </p>
<h5>Certificate Authorities</h5>
<p>Actor hoặc một node có thể tham gia vào mạng blockchain, thông qua digital identity bởi một hệ thống cơ quan tin cậy. Trong đa số các trường hợp, digital identities có dạng chứng chỉ kỉ thuật số được mã hoá tuân theo chuẩn X.509 và được phát hành bởi một Certificate Authority (CA)</p>
<p>CA là một phần phổ biến của các giao thức bảo mật internet và bạn có lẽ nghe về một vài cái phổ biến hơn:  Symantec, GeoTrust, DigiCert, GoDaddy, Comodo,...</p>
<img src="http://sv1.upsieutoc.com/2018/06/28/Screenshot-from-2018-06-28-22-52-23.png" />
<p>Chứng chỉ được ký bởi CA và trói buộc actor với public key của nó. Chứng chỉ có thể được phổ biến rộng rãi vì chúng không bao gồm khóa riêng của tác nhân cũng như khóa riêng của CA. Vì vậy, chúng có thể được sử dụng như là neo của tín thác để xác thực tin nhắn đến từ các diễn viên khác nhau.</p>
### Root CAs, Intermediate CAs and Chains of Trust
<p>CA có 2 loại: Root CAs và Intermediate CAs. Bởi vì Root CAs phân phối hàng trăm triệu chứng chỉ cho người sử dụng, nên nó chia ra cho các intermediate xử lý. Mỗi Intermediate lại cung cấp nhiều chứng chỉ cho tổ chức. Cách làm này sẽ đảm bảo bảo mật hơn, vì ít tác động đến Root CA</p>


