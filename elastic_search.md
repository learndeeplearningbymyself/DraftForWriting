Elastic Search Practice guide

Tham khảo từ [sách](https://www.amazon.co.jp/Elasticsearch%E5%AE%9F%E8%B7%B5%E3%82%AC%E3%82%A4%E3%83%89-impress-top-gear-%E6%83%A3%E9%81%93/dp/4295003913/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=2CG94FTBJVCZN&keywords=elasticsearch+%E5%AE%9F%E8%B7%B5%E3%82%AC%E3%82%A4%E3%83%89&qid=1566870901&s=gateway&sprefix=elasticsea%2Caps%2C237&sr=8-1)

**2.1. Concepts cơ bản**

- Đơn vị lưu trữ cơ bản là **document** ~= **record** trong **table**, nhưng lưu dưới dạng JSON
Khi đưa vào ElasticSearch các document đều được thêm 1 trường để quản lí đó là **ID**
- Dưới document là **field** - tương đương 1 cặp **key - value**

Khi tiến hành search bằng ElasticSearch đa phần đều search trên field, quá trình index cũng diễn ra trên field

- Kiểu dữ liệu **text** khi lưu trữ sẽ đươc cho đi qua bộ **Analyzer** để tách thành các **tokenizer**
- Kiểu dữ liệu **keyword** thì không bị tokenize mà sẽ được giữ nguyên và tìm kiếm theo *nguyên khối*. VD:

> taro.yamada@example.com

sẽ không bị tìm kiếm theo từng thành phần như **yamada** hay **example.com** mà sẽ là cả khối **taro.yamada@example.com**

- **index** - gồm 2 ý nghĩa
  - Nơi lưu trữ document
  - Tách document (tuỳ theo analyzer) -> cấu thành thông tin **transpose index**, quá trình lưu index là việc 1 số lượng **shard** nhất định được phân chia và l**ưu trữ phân tán trên các nodes**

- **document type** - cho biết document được tạo nên từ fields nào (tuỳ vào tính chất của document)
VD: với bài viết blog thì các thuộc tính cần có là: **nội dung chính**, **ngày đăng**, **người tăng**, ...

- **mapping** - ghi lại thông tin về **kiểu dữ liệu**, **cấu trúc dữ liệu** của các fields trong document, với elasticsearch không nhất thiết phải định nghĩa **mapping** từ trước mà thay vào đó, elasticsearch sẽ tự động đoán biết được kiểu dữ liệu và **tự động định nghĩa mapping** sau đó sẽ lưu trữ document

- **node** ở đây là các server mà Elasticsearch (ES) hoạt động, ES chạy trên máy ảo JVM (mỗi một instance của JVM sẽ gọi là node). Phương pháp deploy điển hình là khởi động 1 node duy nhất trên các OS của các Server vật lí (hoặc ảo hoá)
  - Các nodes đều có 1 tên duy nhất (node.name) - cũng là tên file config của node

- **cluster** - là tập các nodes được gộp lại thành 1 nhóm (khi khởi động ES, có nhiều nodes cùng khởi động, chúng sẽ gửi tin nhắn qua lại và tự thiết lập nhóm)
  - Các clusters đều có 1 tên phân biệt (unique) là **cluster.name**
  - với các nodes group có cùng **cluster.name** chúng sẽ được coi nhưng chung 1 cluster và ngược lại

- **shard** - dữ liệu được đánh index trong ES sẽ được lưu (phân tán) trên nhiều nodes khác nhau (chúng được sao lưu thành nhiều bản - mỗi bản này gọi là shard)
  - Thực thể của các shards chính là các **index files Lucence** được tạo ra trên các node
  - ES sẽ liên kết các nodes lại với nhau cho mục đích tìm kiếm, lưu trữ (trên các **lucence files**)
  - Cần chỉ ra **số lượng shards** khi đánh index
  - Nhưng không thể tăng số lượng shard sau khi index (cần dự ước số lượng shard từ trước)

- **Replica** - là **cơ chế duplication tự động** các shard của ES. Shard gốc được sử dụng làm source cho quá trình duplication gọi là **primary shard**, các shard đươc duplicate gọi là **Replica shard**
  - Khi index thay đổi thì **primary shard** sẽ thay đổi đầu tiên, sau đó chuỗi các **replica shards** cũng sẽ được phục chế theo đó
  - Để tăng tính khả dụng thì hai loại **primary shard** và **replica shard** không nên được gán cho nhau. Vì khi

> Node bị hỏng -> shard bị mất -> 1 replica shard sẽ được chọn thay cho primary shard 1 cách tự động

Việc có nhiều replica cũng giúp tăng khả năng xử lí song song. Có thể thay đổi số lượng replica sau khi index

Mô hình của 1 cluster:

<img src="https://user-images.githubusercontent.com/43769314/63745567-80752800-c8dd-11e9-8f76-9f5758cd8e52.png" width="720">

**2.2. Cấu trúc hệ thống**

ES có cấu trúc phân tán, các clusters chứa các nodes (các nodes sẽ liên kết, liên lạc, gửi tin cho nhau cũng như có vai trò kế thừa nhau)

**Node Type** - có 4 loại nodes
- Master
- Data
- Ingest
- Coordinating

Default setting nodes thường đảm nhận vai trò của **master**, **data** và **ingest** node

Với các hệ thống quy mô nhỏ thường sẽ thấy 1 ~ vài **default setting nodes** tuy nhiên khi số lượng nodes tăng lên thì vai trò của 1 node sẽ được phân tán và chia thành nhiều nodes con hơn (mỗi node sẽ đảm nhận 1 nhiệm vụ riêng biệt)

**Masterーnode** - có vai trò quản lí trong 1 cluster, nó sẽ đảm nhận các nhiệm vụ như sau
- Quản lí node tham gia và rời khỏi cluster: bằng cách gửi **ping** đến các nodes còn lại, dựa vào việc có/ không có phản hồi để nhận biết node còn hoạt động hay không

- Quản lí metadata của cluster: số lượng nodes, shards, mapping, index, .... Truyền đạt thông tin thay đổi cho các nodes khi cần

- Gán và sắp xếp, bố trí các shards

Khi **master node** ngừng hoạt động thì các tính năng của ES cũng ngừng theo vậy nên trong hệ thống cần có các **nodes master dự phòng**, các nodes này gọi là **master-eligible node**

Mặc định mọi node sẽ là **master-eligible** nhưng có thể thiết lập để chỉ có 1 hoặc 1 vài node chọn làm **master-eligible** bằng cách chỉnh sửa file setting **elasticsearch.yml** của node như sau

```javascript
node.master: true
node.data: false
node.ingest: false
```

Mặc định cả 3 giá trị trên đều là **true**

**Data-node**: Có nhiệm vụ lưu trữ dữ liệu, xử lí, trả lời query, quản lí các **index files Lucence**
Sau khi client đánh index cho document thì sẽ quyết định shard nào sẽ lưu trữ, sau đó sẽ tiến hành routing đến Data node nào mang số hiệu shard đó.

<img src="https://user-images.githubusercontent.com/43769314/63750012-91c33200-c8e7-11e9-902c-8299c0a6ad9d.png" width="720">

Có 2 pha:
- **scatter** - routing đến node chứa nhiều hơn 1 shard để xử lí nội dung query
- **gather** - tập hơp response từ các nodes

<img src="https://user-images.githubusercontent.com/43769314/63752172-bcaf8500-c8eb-11e9-8b2a-b0474cdb9cc6.png" width="720">

Mặc định mọi nodes đều mang vai trò của **Data node**, ta có thể thay đổi vai trò đó tương tự như với **master node** với

```javascript
node.master: false
node.data: true
node.ingest: false
```

**Ingest-node** - tiền xử lí dữ liệu trước khi được đánh index theo cơ chế pipeline (tuỳ từng tình huống có thể sử dụng pipeline hoặc không). Mặc định mọi nodes có thể đảm nhận vai trò của **ingest-node** những cũng có thể thiết lập qua file **elasticsearch.yml**

```javascript
node.master: false
node.data: false
node.ingest: true
```

**Coordinating-node** - chỉ tiến hành điều phối request từ client đến các shard (**scatter** & **gather**), thiết lập cũng tương tự 3 loại trên

```javascript
node.master: false
node.data: false
node.ingest: false
```

<img src="https://user-images.githubusercontent.com/43769314/63756054-ace76f00-c8f2-11e9-8038-1e0247e2d3b5.png" width="720">

Dùng để phân tải cho quá trình xử lí request cũng như xử lí thống kê kết quả tìm kiếm (tránh để **Data node** đảm nhiệm)

**Việc chọn master node**

Để đảm bảo tính khả dụng của hệ thống nên chọn từ **3 master-eligible nodes trở lên**
