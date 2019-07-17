## OAuth cơ bản

**Tham khảo**
- http://bluzky.github.io/post/2018-01-21-tim-hieu-oauth/
- https://kipalog.com/posts/Tro-lai-co-ban--Oauth-2

### Tổng quan

OAuth không chỉ là **protocol** mà nó còn là một **framework**, đòi hỏi implement ở cả **server** lẫn **client**

### Cơ chế

Ở đây chỉ trình bày về OAuth2.0. Có 3 bên:
- Ứng dụng **bên thứ 3** có sử dụng social network API (**facebook**, **twitter**)
- Người dùng ứng dụng
- Social network - bên cung cấp API, cũng như đảm nhận chứng thực cho OAuth

<img src="https://user-images.githubusercontent.com/43769314/61342703-169d4380-a886-11e9-87e7-b2548d2ba739.png">

Ở hình trên:
- **Client** là ứng dụng bên thứ 3 sử dụng **social network api**
- **Resource owner** là người dùng có tài khoản **social network**
- OAuth2.0 có sự tách biệt giữa **Authorization Server** và **Resource Server**

Cơ chế của OAuth khá dễ hiểu
- B1: Ứng dụng hỏi người dùng quyền truy cập một số tài nguyên trên **social network** của người dùng
- B2: Người dùng đồng ý thông qua một giao diện do phía **social network** cung cấp
- B3: Ứng dụng nhận được một **key** từ phía **social network**
- B4: Ứng dụng sử dụng **key** đó để truy cập một số tài nguyên của người dùng trên **social network**

### OAuth 3-legged, OAuth 2-legged

Xét **Client Credential Flow** đây là quá trình để cho bên cung cấp dịch vụ (facebook, twitter) biết được là người dùng đã cho phép ứng dụng bên thứ 3 truy cập vào tài nguyên của người dùng trên dịch vụ (facebook, twitter, ..)

Quá trình này có thể diễn ra tại 2 thời điểm:
- Tại lúc mà ứng dụng hỏi người dùng
- Hoặc **trước**

Sự khác biệt về mặt thời điểm này đã nảy sinh 2 khái niệm **3-legged** hoặc **2-legged** như trên

#### OAuth 3-legged

Đây là mô hình được sử dụng nhiều nhất cho OAuth2.0. **Client Credential Flow** được thực hiện thông qua việc điều hướng ngời dùng đến một trang xác nhận có đồng ý cho phép ứng dụng bên thứ 3 truy cập tài nguyên của người dùng trên **service** đó hay không. Nếu người dùng cho phép, sẽ điều hướng người dùng tới **URL** đã thiết lập với **Service Provider API** kèm theo **access token** từ phía **service provider**

Sau đó ứng dụng bên thứ 3 sẽ sử dụng **token** để truy cập thông tin người dùng.
Flow chứng thực này yêu cầu 3 bên nên gọi là **3-legged**

Hình minh hoạ

<img src="https://user-images.githubusercontent.com/43769314/61344695-25d3bf80-a88d-11e9-8551-3718ad6bf799.png">

#### OAuth 2-legged

Nếu ứng dụng bên thứ 3 có độ tin tưởng cao, hoặc trước đó khi cài đặt, ... người dùng đã cho phép quyền thì việc "điều hướng 3 bên" như trên là không cần thiết, lúc này chỉ có **ứng dụng** và **service provider** thoả thuận với nhau nên gọi là **2-legged**

Hình minh hoạ

<img src="https://user-images.githubusercontent.com/43769314/61344861-c2965d00-a88d-11e9-9ea6-1fd6eb07d9a8.png">
