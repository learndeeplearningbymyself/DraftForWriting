## AWS Quick Note

Tham khảo từ các nguồn:
- https://qiita.com/shibataka000/items/e3f3792201d6fcc397fd

### 1. Amazon Cognito

Cung cấp **authentication**, **authorization** và **user management** với web, mobile app

Gồm 2 phần:
- User pool - là các **user directories** cung cấp **signin**, **signup** options cho users.
  - Bản chất là user directory, mỗi member sẽ có 1 profile directory mà ta có thể truy cập thông qua SDK
- Identity pool - cho phép phân quyền access của user đối với các AWS services
  - Có thể được sử dụng để lấy về **temporary AWS credential** cho mục đích access các AWS services khác
  - Cần tích hợp với **User pool** để lưu trữ **user profile information**

Cơ chế hoạt động
1. Đăng nhập thông qua **user pool**, **user pool** sẽ cung cấp **user pool token** (bản chất là JSON web tokens - JWT) cho phía user nếu đăng nhập thành công
2. Tiếp theo, hoán đổi giữa **token** và **AWS credentials** thông qua **identity pool**
3. Sử dụng **AWS credential** này để truy cập vào các **AWS Services**

### 2. DynamoDB

Một dạng database (key-value) - NoSQL, ưu tiên tính mở rộng cao

### 2.1. Partition Key
Dữ liệu trong DynamoDB được lưu phân tán trên nhiều partitions khác nhau. Việc dữ liệu được lưu ở partition nào sẽ được định nghĩa thông qua **partition key**

Trong partition có **sort key** thì dữ liệu cũng có thể được sắp xếp

Xét ví dụ dưới: Với bảng Pets, ta có **partition key** là **AnimalType** và **sort key** là **Name**

<img src="https://camo.qiitausercontent.com/8cd0a0437e865d14eef0e14960204b306c6cf2d6/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f36313634312f62306133326162322d383061312d633763302d353464372d3333386130346636623135362e706e67" width="720">

Nguồn: https://qiita.com/shibataka000/items/e3f3792201d6fcc397fd

### 2.2. Các API dùng với DynamoDB

- Tạo dữ liệu:
  - **PutItem** - Ghi dữ liệu (1 record) với **Primary Key** chỉ định trước
  - **BatchWriteItem** - Ghi dữ liệu theo batch
- Đọc/ lấy dữ liệu:
  - **GetItem** - Lấy dữ liệu (1 record), có chỉ ra **Primary Key**
  - **BatchGetItem** - Lấy dữ liệu theo batch
  - **Query** - Lấy (nhiều) dữ liệu thông qua việc chỉ định **Partition Key**, chỉ định **Sort Key** để filter dữ liệu thu được
  - **Scan** - Lấy về toàn bộ dữ liệu của bảng
- Cập nhật dữ liệu:
  - **UpdateItem** - Update dữ liệu (1 record) thông qua việc chỉ định **Primary Key**
- Xoá dữ liệu:
  - **DeleteItem** - Xoá dữ liệu (1 record) thông qua việc chỉ định **Primary Key**
  - **BatchWriteItem** - Xoá dữ liệu theo batch
