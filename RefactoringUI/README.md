#### What you actually need

Thực tế là chúng ta cần một tập hợp màu toàn diện hơn thế này cho giao diện của trang web

<img width="720" src="https://user-images.githubusercontent.com/15076665/69809518-40e81000-122d-11ea-848b-b510d99e575e.png">

Chúng ta có thể chia bảng màu trên thành 3 loại chính sau:

**Grey**
Text, backgrounds, panels, form controls thường sẽ có màu **Grey**

<img width="720" src="https://user-images.githubusercontent.com/15076665/69809672-8c9ab980-122d-11ea-8d14-8a54dfdd42bb.png">

Thực tế chúng ta sẽ cần **8-10 shades** cho màu grey như thế này, vì đôi khi chúng ta muốn màu đậm hơn **light grey** một chút, ...

<img width="720" alt="Screen Shot 0031-11-28 at 22 24 27" src="https://user-images.githubusercontent.com/15076665/69809816-e00d0780-122d-11ea-9a9d-d6a8efa4816c.png">

Bắt đầu với **true black** sẽ tạo cảm giác mất tự nhiên, vậy bạn nên bắt đầu từ **dark grey** và tăng độ sáng lên dần.

**Primary color(s)**
Đây là màu chủ đạo của sản phẩm, có thể coi như một *nhận diện thương hiệu*, thương sẽ có 1, 2 màu chính. Tương tự như grey ta cũng cần 5-10 shades (lighter-darker) cho màu chính này.

<img width="720 src="https://user-images.githubusercontent.com/15076665/69810564-8e657c80-122f-11ea-862f-7f9404ad26a1.png">

**Ultra-light shades** sẽ dùng cho **background** của **alert**, còn **darker shade** sẽ dùng cho **text**

**Accent colors**
Sử dụng những màu này để thu hút sự chú ý của người dùng (ví dụ như dùng cho các feature mới)

<img width="670" src="https://user-images.githubusercontent.com/43769314/69935607-c105c280-1518-11ea-813c-77ea3d8312f6.png">

Ngoài ra chúng ta cũng cần các màu để nhấn mạnh vào các states khác nhau ví dụ như

- Màu đỏ cho các hành động xoá, huỷ:

<img width="660" src="https://user-images.githubusercontent.com/43769314/69935763-307bb200-1519-11ea-9482-7c6eaf8c764d.png">

- Màu vàng cho warning message:

<img width="670" src="https://user-images.githubusercontent.com/43769314/69935786-3d000a80-1519-11ea-8eff-3a7c97527f94.png">

- Màu xanh cho các positive trend:

<img width="660" src="https://user-images.githubusercontent.com/43769314/69935794-46897280-1519-11ea-8a2f-2fe65e71f2c4.png">

Với mỗi màu nên có từ 5-10 **shades**, chúng ta sẽ cần nhiều accent color khi xây dựng những thành phần cần có sự phân biệt (VD: lines trong đồ thị, events trong lịch, tags trong project)

### Define your shades up front

Khi bạn cần tạo các màu đậm hoặc nhạt hơn trong palette của bạn, đừng sử dụng các tiếp đầu ngữ như *darker* hoặc *lighter* vì cuối cùng bạn cũng sẽ chỉ tạo ra một mớ bùng nhùng với các màu "same same" nhau. Thay vào đó hãy tạo một tập cố định các shades như sau:

<img width="680" src="https://user-images.githubusercontent.com/43769314/69936572-82bdd280-151b-11ea-9171-f7c2571a16c4.png">

Nhưng làm cách nào để tạo được 1 palette như vậy ?

#### Choose the base color first

Đầu tiên chọn một màu cơ bản để nó có thể "đứng giữa" các sắc độ đậm, nhạt khác

Trên thực tế, không có cách nào hoàn hảo để làm việc này tuy nhiên với **primary color** và **accent color** ta sẽ chọn các màu phù hợp để làm button background

<img width="680" src="https://user-images.githubusercontent.com/43769314/69937767-f4e3e680-151e-11ea-93ac-3671dd34257f.png">

Điều quan trọng nhất cần chú ý là không có luật là "bắt đầu với 50% nhạt hơn" hoặc bất cứ thứ gì khác - mọi màu đều có sự khác biệt, bạn chỉ có thể dựa vào con mắt của mình mà thôi

#### Finding the edges

Chọn sắc độ (shade) tối và sáng nhất. Điều này giúp cho bạn có thể nghĩ về ngữ cảnh cũng như trường hợp sử dụng chúng

- Sắc độ tối nhất của một màu thường dùng cho text
- Sắc độ sáng nhất thường dùng cho background của element

Một alert đơn giản sẽ là một ví dụ tốt cho việc kết hợp 2 sắc độ trên

<img width="570" src="https://user-images.githubusercontent.com/43769314/69938666-3d040880-1521-11ea-854a-f54abd9cc0c1.png">

Bắt đầu với một màu trùng sắc độ **hue** với màu base của bạn, thay đổi **saturation** và **lightness** đến khi bạn hài lòng thì thôi.

#### Filling in the gaps

Sau khi đã có base color, darkest và lightness, chúng ta cần hoàn thiện các màu ở giữa. Với các projects, ít nhất sẽ có 5 shapes và nhiều nhất là 10 shapes, tuy nhiên 9 shapes là một con số vừa đẹp vì nó có sự phân chia tốt hơn các con số còn lại cũng như đảm bảo đầy đủ số lượng shapes cho màu.

<img width="500" src="https://user-images.githubusercontent.com/43769314/69939287-d8e24400-1522-11ea-9f44-83ad6b04b888.png">

Màu darkest sẽ là **shade 900**, lightess sẽ là **shade 100**, ta sẽ *điền* các màu với sắc độ *700* và *300* sao cho chúng dung hoà (trung bình) so với 2 màu ở 2 biên

<img width="480" src="https://user-images.githubusercontent.com/43769314/69939316-e697c980-1522-11ea-96f9-bd6958c8de56.png">

Các shade còn lại sẽ được điền đầy theo một cách làm tương tự trên

<img width="480" src="https://user-images.githubusercontent.com/43769314/69939359-029b6b00-1523-11ea-8c42-1f3c2a7e915b.png">

Chúng ta nên tạo ra một tập màu với một mức độ cân bằng nhất định, đủ cho ý tưởng thiết kế mà không cảm thấy bị giới hạn

#### What about greys?

Với grey thì base color không quá quan trọng nhưng cách làm hoàn toàn tương tự trên. Tuy nhiên ta sẽ chọn lấy màu darkest là màu darkest của text, còn màu lightest sẽ là màu hoạt động tốt ở các background sáng màu.

<img width="630" src="https://user-images.githubusercontent.com/43769314/69940244-252e8380-1525-11ea-86d3-d9007b45e77e.png">

#### It’s not a science

Trong thực tế không có một công thức hay con số cụ thể nào cho việc tạo palette color nhưng hãy tuân thủ theo như cách làm trên, cũng như hạn chế việc thêm các shade mới nhiều nhất có thể, nếu như thêm quá nhiều shades, bạn sẽ không bao giờ có được một palette màu mong muốn.

> Việc chỉnh sửa saturation cũng như lightness là chuyện hoàn toàn bình thường, đừng ngại ngần chỉnh sửa sao cho phù hợp nhất với con mắt của bạn

### Don’t let lightness kill your saturation



