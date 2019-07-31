## Emphasize by de-emphasizing

Đôi lúc bạn muốn nhấn mạnh vào 1 item nào đó, nhưng không phải lúc nào muốn **nhấn mạnh cũng được** như ví dụ dưới đây

<img src="https://user-images.githubusercontent.com/43769314/62177971-f7bca800-b381-11e9-97c0-e6fc82fe5d0b.png" width="720">

Dù ta có nhấn mạnh **active nav item** thì nó trông cũng không khác nhiều so với các inactive item còn lại. Trong những tình huống thế này thay vì cố gắng nhấn mạnh item chính ta có thể làm mờ (de-emphasize) các item xung quanh như dưới đây

<img src="https://user-images.githubusercontent.com/43769314/62178091-7f0a1b80-b382-11e9-9268-e1262a3d2499.png" width="720">

Ta để cho màu của các items xung quanh chìm xuống màu của background
Ta cũng có thể áp dụng cách này đối với những phần UI lớn hơn như ví dụ sau: khi phần sidebar khiến cho nội dung chính của trang không được nổi bật thì ta có thể bỏ đi background của sidebar để nội dung của nó hiển thị trực tiếp trên background

<img src="https://user-images.githubusercontent.com/43769314/62178956-c34aeb00-b385-11e9-820a-5fde97997f5e.png" width="720">

## Labels are a last resort

Khi hiển thị dữ liệu lấy ra từ database, chúng ta thường sử dụng format

> label: value

Rất nhiều người mắc phải *bẫy* này, việc hiển thị thông tin theo kiểu này sẽ khiến người đọc khó nắm bắt thông tin do **không hề có bất cứ một hệ thống phân cấp thông tin** nào ở đây - mọi phần của thông tin đều có cùng một ấn tượng như nhau (thiếu đi điểm nhấn đặc trưng)

### You might not need a label at all

Trong nhiều tình huống khi nhìn vào nội dung người đọc có thể hiểu ngay lập tức ý nghĩa của nó cũng như việc **nó là gì**. Ví dụ:
- abc@mail.com => email
- 01923-12312-12312 => số điện thoại
- Michael Ng => tên

Khi format là chưa đủ, hãy để cho ngữ cảnh lên tiếng. Ví dụ như: khi vào trang tin về nhân sự một công ty, nếu thấy dòng chữ "Customer support" nằm phía dưới tên của một người thì ta có thể kết luận đó là vị trí của người đó trong công ty mà không cần đến *sự liên kết* của label

<img src="https://user-images.githubusercontent.com/43769314/62182042-3bb6a980-b390-11e9-8a38-758bc7ce5848.png">

Khi có thể hiển thị dữ liệu mà không cần label, ta có thể khiến cho giao diện dễ nhìn hơn cũng như có thể **nhấn nhá** và **đảm bảo yếu tố căn gióng**

### Combine labels and values

Khi kết hợp 2 yếu tố label và value lại với nhau ta nên tìm cách làm rõ (nhấn mạnh) value. Như ở hình bên dưới thay vì nói: "In stock: 12" thì ta nên nói "12 in stock"

<img src="https://user-images.githubusercontent.com/43769314/62185372-24ca8400-b39d-11e9-8eb0-27a7c7c0652f.png" width="720">

Nếu như tìm cách kết hợp được 2 yếu tố trên nhưng vẫn đảm bảo tính rõ ràng của value thì sẽ tốt hơn nhiều so với việc cố gắng **làm rõ** ý nghĩa của từng thành phần label hay value

### Labels are secondary

Đôi khi chúng ta thực sự cần label, như trong trường hợp của giao diện dashboard khi có khá nhiều dữ liệu và format của chúng cũng gần như nhau nên việc sử dụng label là một ý tưởng hay giúp người đọc dễ dàng nắm bắt nội dung

Thế nhưng, ta cũng có thể coi label trong trường hợp này như một dạng supporting content, de-emphasize chúng (lighter font weight, reduce constrast, ...) và làm nổi bật nội dung (dữ liệu)

<img src="https://user-images.githubusercontent.com/43769314/62186062-c9e65c00-b39f-11e9-810d-1116b52b8329.png" width="720">

### When to emphasize a label

Có những tình huống người dùng quan tâm đến label hơn là dữ liệu. Ví dụ khi người dùng đang tra cứu một trang thuộc dạng **information-dense** (trang thông tin về kĩ thuật) thì việc nhấn mạnh vào label là cần thiết

Vì khi người dùng muốn tìm kiếm chiều dày của điện thoại thì yếu tố mà người dùng muốn quét qua là từ khoá **depth** chứ không phải giá trị của nó là **8mm**

Tuy nhiên dữ liệu vẫn là thông tin quan trọng, ta có thể làm nổi bật label bằng font-weight đậm hơn một chút và dữ liệu nhẹ đi một chút là vừa đủ

## Separate visual hierarchy from document hierarchy

Với các nội dung có tính ngữ nghĩa - như đoạn văn chẳng hạn, việc sử dụng các thẻ title: h1, h2, h3, ... là điều khá phổ biến. Tuy nhiên chúng ta được dạy rằng **title** thường sẽ có kích cỡ lớn hơn phần còn lại

Thế nhưng yếu tố ta muốn tập trung ở đây không phải là title mà là content. Thế nên trong nhiều trường hợp, title sẽ chỉ đóng **vai trò như label** mà thôi. Điều đó cho thấy không phải lúc nào title có kích cỡ lớn cũng là hợp lí, mà bản thân nội dung cũng có thể nói lên tất cả

<img src="https://user-images.githubusercontent.com/43769314/62189802-e76cf300-b3aa-11e9-84eb-837a008fbe06.png" width="720">

> Đừng để element đang sử dụng làm ảnh hưởng đến việc style cho thiết kế

## Balance weight and contrast

Ta có thể thấy rõ các **font bold** thường nổi bật hơn **font regular** là vì chúng chiếm nhiều diện tích bề mặt hơn dẫn đến việc sử dụng nhiều pixels hơn

### Using contrast to compensate for weight

Một ví dụ điển hình đó là khi kết hợp **text** và **icon**. Chúng ta có thể thấy điều hiển nhiên là icon sẽ nổi bật hơn text khi chúng đi cùng nhau (đặc biệt là solid icons)

Tuy nhiên với icon ta không thể xử lí bằng cách chỉnh weight, cách thích hợp nhất đó là sử dụng màu nhạt hơn (so với text) cho icon

<img src="https://user-images.githubusercontent.com/43769314/62194093-19368780-b3b4-11e9-8088-17dcc7a779d8.png" width="720">

Đây là một cách khá hay khi xử lí các elements có cùng weight, giảm đi tương phản, khiến cho các elements nặng hơn có **cảm giác nhẹ đi** mà không thay đổi weight

### Using weight to compensate for contrast

Giống như việc giảm tương phản để de-emphasize element thì ta cũng có thể tăng weight để nhấn mạnh vào những element có độ tương phản thấp

Điều này khá hữu hiệu khi sử dụng những bo viền có tương phản thấp và khá mỏng (1px), nếu làm cho bo viền màu tối sẽ khiến người dùng tập trung quá nhiều vào bo viền thay vì nội dung chính, còn nếu dùng màu quá nhạt thì ý nghĩa ngăn cách của bo viền sẽ giảm

<img src="https://user-images.githubusercontent.com/43769314/62197592-13907000-b3bb-11e9-8e53-94865dbd9936.png" width="720">

Có thể tăng nhấn nhá cho bo viền bằng cách tăng độ rộng (tăng weight) khi đó vẫn giữ nguyên được màu sắc

<img src="https://user-images.githubusercontent.com/43769314/62197749-64a06400-b3bb-11e9-8c83-810b9064501a.png" width="720">

## Semantics are secondary

Chúng ta thường mắc vào bẫy *thiết kế các actions theo semantics* mà quên đi tính kế thừa của chúng

Trong các pages thì hầu như chỉ có:
- 1 main action
- 2 secondary actions
- Một vài các actions phụ khác

Nếu thiết kế theo semantics thì sẽ trông như sau

<img src="https://user-images.githubusercontent.com/43769314/62200702-ee9efb80-b3c0-11e9-982a-5c92cc9bb22f.png" width="720">