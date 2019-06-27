## GraphQL Tutorials

Nguồn: https://www.howtographql.com/basics/0-introduction/

### Introduction
- Là 1 chuẩn API
- Cho phép **declarative data fetching**, tức client có thể chỉ ra chính xác dữ liệu nào cần thiết thông qua API
- GraphQL đưa ra 1 endpoint duy nhất và responds lại đúng dữ liệu mà client cần
- GraphQL giảm thiểu tối đa lượng dữ liệu truyền qua network qua đó cải thiện application operation

### GraphQL is the better REST
-  GraphQL được phát triển với mục đích tăng tính flex và hiệu quả trong giao tiếp giữa client và server
- Khái niệm **endpoint** ở đây có thể hiểu như là **API endpoint** (VD: /user/id)
- Ta xét 1 VD đơn giản như sau: cần xây dựng 1 blogging app, cụ thể là xây dựng trang cá nhân của 1 người dùng. Trong trang này ta muốn hiển thị: Tên người dùng, Danh sách title của các bài posts của người dùng và 3 người theo dõi gần đây nhất của người dùng hiện tại. Có thể liệt kê 3 API endpoint mà client sẽ sử dụng như sau:
  - **/users/id** (thông tin cá nhân của người dùng), **/users/id/posts** (danh sách bài posts của người dùng), **/users/id/followers** (danh sách người theo dõi của người dùng hiện tại)
  - Nếu chỉ sử dụng REST API thì lượng thông tin thừa fetch về phía client là khá nhiều (VD: dữ liệu cá nhân của người dùng, ngoài tên còn có thể có **ngày sinh, địa chỉ, ...**, tương tự với **posts API** và **followers API**)
  - Nếu không thực hiện theo chuẩn **REST** thì cứ mỗi khi **UI Design** bên phía client thay đổi thì ta buộc phải thay đổi cấu trúc của **API** từ đó dẫn đến việc mất thời gian trong quá trình xây dựng ứng dụng
- Với GraphQL chỉ cần 1 endpoint duy nhất là có thể lấy về **chỉ những dữ liệu cần thiết**
- Bản chất ở đây là client sẽ gửi cho server `1 POST request` duy nhất, request này sẽ chứa câu truy vấn dữ liệu mà client cần sử dụng và sau đó trả về cho client dữ liệu dưới dạng JSON
- **Không còn tình trạng Over - and Underfetching**
  - **Overfetching** - là việc kéo về những dữ liệu không cần thiết
  - **Underfetching** - là trường hợp ngược lại, các endpoints không trả về đủ dữ liệu cần thiết nên client phải gửi thêm các requests khác tới server, dấn đến tình trạng **n + 1 requests problem**

- **Rapid Product Iterations**
  - Với REST: cấu trúc của endpoint sẽ phải thay đổi theo dữ liệu mà client cần
  - Với GraphQL: không cần chỉnh sửa API khi product requirements và thiết kế thay đổi, có thể ứng phó nhanh với user feedback

- GraphQL sử dụng **type system** để định nghĩa khả năng vcủa API
- **Schema** hoạt động như một cầu nối giữa client và server -> giúp team dev 2 bên có thể hoạt động độc lập với nhau

### Core Concepts
- The Schema Definition Language (SDL)
  - Sử dụng SDL để định nghĩa **type**
 ```
 type Person {
    name: String!
    age: Int!
 }

 type Post {
    title: String!
 }
 ```
  - Kí hiệu **!** chỉ ra rằng property là bắt buộc
  - Sử dụng SDL để định nghĩa **relation** (quan hệ giữa các types)
```
type Person {
    name: String!
    age: Int!
    posts: [Post!]!
}

type Post {
    title: String!
    author: Person!
}
```
  - Dữ liệu trả về từ GraphQL là không cố định như REST API
```
{
    allPersons {
        name
    }
}
```
  - Trong ví dụ trên `allPersons` gọi là **root** của query, tất cả mọi thứ đi sau **root** của query gọi là **payload** của query
```
{
    allPersons {
        name {
            posts {
                title
            }
        }
    }
}
```
  - Ở ví dụ trên, ngoài việc fetch name của user, ta còn tiến hành fetch cả posts (kèm title) của user
- Mutation: là khái niệm dùng khi muốn thay đổi dữ liệu có trong DB, có 3 loại mutations
  - **creating** new data
  - **updating** existing data
  - **deleting** existing data
```
mutation {
    createPerson(name: "Bob", age: 36) {
        name
        age
    }
}
```
- Trong ví dụ trên, ta thêm từ khoá **mutation** ở đầu, truyền thêm tham số **name**,**age** cho **root** là **createPerson**, trong **payload** ta cũng sẽ chỉ ra các fields tương ứng
- Giá trị trả về sẽ là
```
"createPerson": {
    "name": "Bob",
    "age": 36
}
```
- Kết quả trả về ở trên sẽ **tương ứng với payload** đã gửi lên cho server
- Ngoài ra ta cũng có thể thêm các trường khác vào trong payload của mutation, để có thể lấy thêm các thông tin khác
- Id được tạo ra thường được gen ngẫu nhiên bởi server
- **Realtime Updates with Subscriptions**
  - Ta có thể sử dụng từ khoá **subscription** để cập nhật dữ liệu từ server 1 cách real-time
```
subscription {
    newPerson {
        name
        age
    }
}
```
  - Trong ví dụ trên, ta sẽ theo dõi khi nào có Person mới được add vào DB, lúc đó server sẽ push dữ liệu xuống client
  - Subscription sẽ **stream data** gửi về cho client, cứ mỗi khi có dữ liệu mới thì chúng sẽ được gửi về cho client subscribe

- GraphQL Schema - chỉ ra cách mà client có thể fetch cũng như update dữ liệu, là tập hợp của các **Types** với **root type** tương ứng
  - Mỗi một schema sẽ có các root types định nghĩa entry point của API
```
type Query {}

type Mutation {}

type Subscription {}
```
  - Các root types sẽ lần lượt là **Query**, **Mutation**, **Subscription**

### Big Picture (Architecture)
- GraphQL chỉ đơn thuần là ngôn ngữ định nghĩa, nó sẽ chỉ ra GraphQL server cần có những gì
- Nếu muốn sử dụng GraphQL trong project, ta cần build GraphQL server
- Các kiến trúc thường sử dụng
  - GraphQL server với DB đã kết nối
  - GraphQL server tích hợp với 1 hệ thống có sẵn
  - Hybrid approach với **connected database** và tích hợp với hệ thống có sẵn