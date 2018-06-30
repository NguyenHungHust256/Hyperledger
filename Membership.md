﻿# Membership
<p>Nếu bạn đọc qua tài liệu về identity, bạn đã hiểu cách một PKI có thể cung cấp xác thực định danh thông qua một chuỗi tin tưởng (chain of trust).Bây giờ chúng ta hãy xem những danh tính này có thể được sử dụng như thế nào để đại diện cho các thành viên đáng tin cậy của một mạng blockchain. Đây là nơi một nhà cung cấp dịch vụ thành viên (MSP) đi vào hoạt động - nó xác đinh các Root CAs và Intermediate CAs được tin cậy để xác định các thành viên của miền tin cậy, ví dụ: một tổ chức, bằng cách liệt kê danh tính của các thành viên, hoặc bởi xác định CAs được uỷ quyền để xác thực danh tính hợp lệ cho các thành viên của họ, bình thường thông qua sự kết hợp của cả 2. </p>
<p>Sức mạnh của MSP vượt xa chỉ đơn giản là liệt kê ai là người tham gia mạng hoặc thành viên của kênh. MSP có thể xác định các vai trò cụ thể mà một tác nhân trong phạm vi tổ chức (vd: admins, or các thành viên của một nhóm tổ chức con), và các tập xác định đặc quyền truy câoj trong môi trường mạng và channel (vd: channel admins, readers, writers).</p>
# Mapping MSPs to Organizations
<p>Một tổ chức là một nhóm quản lý thành viên. Nó có thể cái gì đó lớn như là một tập đoàn đa quốc gia hoặc nhỏ như là một cửa hàng hoa. Cái quan trọng nhất của tổ chức là họ quản lý thành viên dưới một single MSP. Chú ý rằng nó khác khái niệm tổ chức định nghĩa ở một bằng chứng X.509.</p>
<p>Mối quan hệ độc quyền giữa một tổ chức và MSP của nó làm nó có tri giác đến tên MSP sau tổ chức, một quy ước bạn sẽ được chấp nhận trong hầu hết cấu hình chính sách. Ví dụ. tổ chức ORG1 có thể sẽ có một MSP được gọi là một cái gì đó như ORG1-MSP. Trong một vài trường hợp, một tổ chức có thể yêu cầu nhiều nhóm thành viên, ví dụ nơi các kênh được sử dụng để thực hiện các chức năng business khác nhau giữa các tổ chức. Trong những trường hợp này, nó có ý nghĩa để có nhiều MSP và đặt tên cho chúng theo đó, ví dụ: ORG2-MSP-NATIONAL và ORG2-MSP-GOVERMENT</p>
<img src="http://sv1.upsieutoc.com/2018/06/29/Screenshot-from-2018-06-29-07-36-47.png" />
<h4>Organizational Units and MSPs</h4>
<p>Một tổ chức thường chia ra nhiều đơn vị tổ chức (organizational units) (OUs), mỗi trong số đó có một bộ trách nhiệm nhất định. Ví dụ, tổ chức ORG1 phải có `ORG1-MANUFACTURING` and `ORG1-DISTRIBUTION` để phản ảnh các dòng tách rời của business. </p>
<p>OUs có thể hữu ích trong việc điều khiển các thành phần của một tổ chức, những cái đuwocj xem xét thành viên của mạng Blockchain. For example, only identities from the `ORG1-MANUFACTURING` OU might be able to access a channel, whereas `ORG1-DISTRIBUTION` cannot.</p>
