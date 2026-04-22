---
layout: default
title: Chính sách Bảo mật — Abba
---

# Chính sách Bảo mật

**Cập nhật lần cuối: 22 tháng 4 năm 2026**

## 1. Giới thiệu

Abba ("chúng tôi", "ứng dụng của chúng tôi", "ứng dụng") là một ứng dụng di động đồng hành trong cầu nguyện và Tĩnh nguyện (Quiet Time) được xây dựng cho các Cơ đốc nhân mong muốn cầu nguyện sâu sắc hơn. Chính sách Bảo mật này mô tả cách Abba thu thập, sử dụng, lưu trữ và bảo vệ thông tin của bạn khi bạn sử dụng ứng dụng iOS (Bundle ID: `com.ystech.abba`).

Abba hiện đang được vận hành như một dự án của nhà phát triển độc lập. Khi chúng tôi đề cập đến "chúng tôi" trong chính sách này, chúng tôi muốn nói đến đội ngũ Abba. Nếu Abba trở thành một công ty đã đăng ký trong tương lai, chính sách này sẽ được cập nhật tương ứng.

Chính sách này áp dụng trên toàn thế giới. Chúng tôi tuân theo các nguyên tắc của Quy định Bảo vệ Dữ liệu Chung của EU (GDPR), Đạo luật Bảo mật Người tiêu dùng California (CCPA) và Đạo luật Bảo vệ Thông tin Cá nhân Hàn Quốc (PIPA) khi áp dụng. Đối với người dùng Việt Nam, chúng tôi tuân thủ tinh thần của Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân.

## 2. Thông tin chúng tôi thu thập

### 2.1 Thông tin tài khoản
Abba là **ẩn danh theo mặc định**. Khi bạn mở ứng dụng lần đầu tiên, chúng tôi tạo một ID người dùng ẩn danh (UUID) để các lời cầu nguyện và cài đặt của bạn có thể đồng bộ giữa các phiên. Bạn không cần cung cấp tên, email hoặc số điện thoại để sử dụng Abba.

Bạn có thể tùy chọn đăng nhập bằng **Apple Sign-In** hoặc **Google Sign-In** để sao lưu dữ liệu. Trong trường hợp đó, chúng tôi nhận địa chỉ email và một định danh duy nhất từ Apple hoặc Google. Bạn có thể sử dụng "Ẩn Email của tôi" với Apple Sign-In nếu muốn.

### 2.2 Nội dung cầu nguyện (Dữ liệu cốt lõi)
Khi bạn sử dụng Abba, chúng tôi thu thập:
- **Bản ghi âm** các lời cầu nguyện được nói ra
- **Bản chép lời** được tạo từ các bản ghi âm đó
- **Văn bản suy niệm và phản ánh** bạn viết hoặc tạo ra
- **Các đoạn Kinh Thánh** bạn đánh dấu

Đây là dữ liệu nhạy cảm nhất mà Abba xử lý, và chúng tôi đối xử với nó một cách cẩn trọng. Âm thanh của bạn được lưu trữ trong thư mục riêng tư của bạn trên kho lưu trữ bảo mật của chúng tôi. Chỉ bạn mới có thể truy cập. Chúng tôi không nghe, không chia sẻ và không sử dụng cho mục đích tiếp thị.

### 2.3 Thông tin đăng ký
Nếu bạn đăng ký Abba Pro, dịch vụ bên thứ ba có tên **RevenueCat** ghi lại trạng thái đăng ký của bạn (đang hoạt động, hết hạn, dùng thử, v.v.) cùng với ID ẩn danh. Chúng tôi **không** nhận số thẻ tín dụng của bạn — thông tin đó được giữ ở Apple.

### 2.4 Thông tin kỹ thuật
- Ngôn ngữ thiết bị (để đặt ngôn ngữ ứng dụng mặc định)
- Nhật ký sự cố với dữ liệu cá nhân được che (qua Sentry)
- Mã thông báo thông báo đẩy (FCM, tùy chọn — chỉ khi bạn bật thông báo)
- Phiên bản ứng dụng và iOS (để gỡ lỗi)

## 3. Cách chúng tôi sử dụng thông tin của bạn

Chúng tôi sử dụng thông tin của bạn để:
- **Cung cấp phân tích AI** cho các lời cầu nguyện và phản ánh Tĩnh nguyện của bạn (Google Gemini)
- **Đồng bộ dữ liệu** giữa các phiên và thiết bị
- **Quản lý đăng ký** và quyền lợi của bạn
- **Sửa lỗi và cải thiện ứng dụng** thông qua báo cáo sự cố
- **Gửi thông báo đẩy tùy chọn** (nhắc nhở Tĩnh nguyện hàng ngày) nếu bạn chọn tham gia

Chúng tôi **không**:
- Hiển thị bất kỳ quảng cáo nào
- Bán dữ liệu của bạn cho bất kỳ ai
- Chia sẻ nội dung cầu nguyện của bạn với bên thứ ba (ngoại trừ việc xử lý AI được mô tả bên dưới)
- Sử dụng nội dung của bạn để đào tạo các mô hình AI

## 4. Dịch vụ bên thứ ba

Abba dựa vào một số dịch vụ đáng tin cậy để hoạt động.

| Dịch vụ | Mục đích | Dữ liệu gửi đi | Khu vực |
|---|---|---|---|
| **Supabase** | Cơ sở dữ liệu & xác thực | ID ẩn danh, lời cầu nguyện, siêu dữ liệu | Mỹ / EU |
| **Google Gemini API** | Phân tích AI các lời cầu nguyện | Chỉ văn bản cầu nguyện | Google Cloud |
| **RevenueCat** | Quản lý đăng ký | ID ẩn danh, biên lai mua hàng | Mỹ |
| **Sentry** | Báo cáo sự cố (đã che PII) | Dấu vết lỗi đã loại bỏ email, bản chép lời dài, JWT | Mỹ / EU |
| **Firebase Cloud Messaging** | Thông báo đẩy (tùy chọn) | Mã thông báo FCM | Google Cloud |
| **Apple Sign-In / Google Sign-In** | Liên kết tài khoản tùy chọn | Email, ID nhà cung cấp | Apple / Google |

**Google Gemini:** Theo chính sách được công bố của Google cho việc sử dụng API trả phí, nội dung cầu nguyện gửi đến Gemini **không được sử dụng để đào tạo các mô hình AI của Google**. Xử lý là tạm thời.

**Che PII của Sentry:** Chúng tôi áp dụng các quy tắc che trước khi gửi báo cáo sự cố — email, bản chép lời dài hơn 50 ký tự, JWT và các định danh khác đều bị loại bỏ.

## 5. Lưu trữ và bảo mật dữ liệu

- Tất cả dữ liệu khi truyền tải được mã hóa qua HTTPS (TLS 1.2+).
- Dữ liệu khi ở trạng thái tĩnh được bảo vệ bằng mã hóa của nhà cung cấp cơ sở dữ liệu.
- **Bảo mật cấp hàng (RLS)** trong Supabase đảm bảo bạn chỉ có thể truy cập dữ liệu của chính mình.
- Tệp âm thanh được lưu trữ trong các thư mục của từng người dùng với quyền truy cập được kiểm soát bởi mã thông báo xác thực của bạn.
- Mã thông báo truy cập được lưu trữ trong Secure Enclave của iOS (`flutter_secure_storage`), không bao giờ ở tùy chọn thông thường.

Chúng tôi giữ dữ liệu của bạn miễn là tài khoản của bạn còn hoạt động. Nếu bạn xóa tài khoản, chúng tôi sẽ xóa dữ liệu của bạn trong vòng **30 ngày**, trừ những trường hợp chúng tôi bị yêu cầu pháp lý phải lưu giữ hồ sơ (như hồ sơ thuế cho các giao dịch mua đăng ký, mà Apple/RevenueCat giữ theo chính sách riêng).

## 6. Quyền của bạn

Bạn có các quyền sau đối với dữ liệu cá nhân của mình:

- **Quyền truy cập** — yêu cầu bản sao dữ liệu chúng tôi giữ về bạn
- **Quyền sửa chữa** — yêu cầu chúng tôi sửa thông tin không chính xác
- **Quyền xóa** — yêu cầu chúng tôi xóa tài khoản và dữ liệu của bạn (có sẵn trong ứng dụng: Cài đặt → Tài khoản → Xóa tài khoản, hoặc qua email)
- **Quyền di chuyển dữ liệu** — yêu cầu xuất dữ liệu của bạn ở định dạng có thể đọc được bằng máy
- **Quyền phản đối** — phản đối một số xử lý nhất định
- **Rút lại sự đồng ý** — bạn có thể rút lại sự đồng ý cho thông báo đẩy, xử lý AI hoặc liên kết tài khoản bất kỳ lúc nào

Đối với cư dân GDPR (EU) và CCPA (California), các quyền này được pháp luật đảm bảo. Để thực hiện bất kỳ quyền nào, gửi email đến **rrallvv@gmail.com**. Chúng tôi phản hồi trong vòng 30 ngày.

## 7. Quyền riêng tư của trẻ em

Abba được xếp hạng 4+ trong App Store. Chúng tôi không cố ý thu thập thông tin từ trẻ em dưới 13 tuổi (COPPA) hoặc dưới 16 tuổi (GDPR, ở một số nước EU) mà không có sự đồng ý xác thực của cha mẹ. Nếu bạn tin rằng một đứa trẻ đã cung cấp thông tin cá nhân, vui lòng liên hệ với chúng tôi và chúng tôi sẽ xóa ngay lập tức.

## 8. Chuyển dữ liệu quốc tế

Cơ sở hạ tầng của chúng tôi được lưu trữ tại Hoa Kỳ và Liên minh Châu Âu. Bằng cách sử dụng Abba, bạn đồng ý với việc dữ liệu của bạn được chuyển đến và xử lý tại các khu vực này. Chúng tôi dựa vào Các Điều khoản Hợp đồng Tiêu chuẩn (SCCs) khi cần thiết.

## 9. Yêu cầu của Chính phủ và Pháp lý

Chúng tôi chỉ tiết lộ dữ liệu người dùng khi pháp luật yêu cầu (trát tòa hợp lệ, lệnh tòa án hoặc tương đương). Chúng tôi chưa công bố báo cáo minh bạch, nhưng cam kết thông báo cho người dùng bị ảnh hưởng khi được pháp luật cho phép.

## 10. Thay đổi đối với Chính sách này

Chúng tôi có thể cập nhật Chính sách Bảo mật này khi Abba phát triển. Khi chúng tôi thực hiện những thay đổi quan trọng, chúng tôi sẽ thông báo cho bạn trong ứng dụng và cập nhật ngày "Cập nhật lần cuối" ở đầu. Việc tiếp tục sử dụng Abba sau khi thay đổi có nghĩa là bạn chấp nhận chính sách đã cập nhật.

## 11. Liên hệ với chúng tôi

Câu hỏi, yêu cầu hoặc khiếu nại?

- **Email:** rrallvv@gmail.com
- **Thời gian phản hồi:** trong vòng 30 ngày (thường sớm hơn)

Bạn cũng có quyền khiếu nại với cơ quan bảo vệ dữ liệu địa phương của mình (ví dụ: DPA của quốc gia thành viên EU, Tổng Chưởng lý California hoặc PIPC của Hàn Quốc).

---
⚠️ **Thông báo Dịch thuật**: Đây là bản dịch được cung cấp cho mục đích thuận tiện.
Trong trường hợp có bất kỳ sự khác biệt nào, [bản tiếng Anh](../privacy.html) sẽ được ưu tiên.
