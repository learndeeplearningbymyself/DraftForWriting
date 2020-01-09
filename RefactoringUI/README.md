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

<img width="720" src="https://user-images.githubusercontent.com/15076665/69810564-8e657c80-122f-11ea-862f-7f9404ad26a1.png">

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

Trong không gian màu HSL, khi lightness gần đến 0% hoặc 100% thì mức độ ảnh hưởng của **saturation** ngày càng giảm - cùng một giá trị **saturation** ở 50% sẽ sống động hơn ở 90%

<img width="350" src="https://user-images.githubusercontent.com/15076665/69961874-232dea00-1550-11ea-97da-764dcc68a735.png">

Điều đó có nghĩa rằng nếu bạn muốn các sắc độ lighter hoặc darker của bạn được rõ nét, hãy tăng giá trị **saturation** của chúng khi lightness ra xa giá trị 50%

<img width="350" src="https://user-images.githubusercontent.com/15076665/69962246-ef06f900-1550-11ea-99cd-e8f730741df3.png">

#### Use perceived brightness to your advantage

<img width="360" src="https://user-images.githubusercontent.com/15076665/69962684-d9de9a00-1551-11ea-928b-3cd2906135e6.png">

Hai màu nàu có cùng brightness nhưng ta vẫn cảm giác màu vàng có vẻ *sáng* hơn, nguyên nhân là do bản thân các màu hue cũng kế thừa những đặc tính sáng/ tối theo cảm nhận của mắt người

Dưới đây là công thức mà bạn có thể sử dụng để tính được độ sáng của một màu RGB

<img width="480" src="https://user-images.githubusercontent.com/15076665/69962888-55d8e200-1552-11ea-95f2-da793f958efb.png">

Với các màu 50% lightness và 100% saturation với hue khác nhau, chúng ta có thể thu về các màu với mức độ sáng khác nhau dọc theo bánh xe màu

<img width="720" src="https://user-images.githubusercontent.com/43769314/70018265-eeaa4480-15c8-11ea-85b2-47d504132e1b.png">

Đúng như mong đợi, màu vàng là màu sáng nhất, tuy nhiên độ sáng không thay đổi một cách tuyến tình từ màu hue tối nhất -> sáng nhất, thay vào đó ta có 3 màu với mức độ sáng *local minimum* (red, green, blue) cũng như 3 màu với mức độ sáng *local maximum* (yellow, cyan, magenta)

#### Changing brightness by rotating hue

Thông thường khi thay đổi độ sáng của màu, chúng ta thường thay đổi **lightness** 

<img width="620" src="https://user-images.githubusercontent.com/43769314/70024986-0d1b3a80-15df-11ea-984d-b4f4146f81d5.png">

Tuy nhiên việc làm này sẽ làm mất đi "cường độ - intensity" của màu khiến cho màu trở nên trắng hơn hoặc đen hơn thay vì sáng hoặc tối hơn.

<img width="330" src="https://user-images.githubusercontent.com/43769314/70025087-553a5d00-15df-11ea-82a2-62936def7ce5.png">

Do bản thân hues cũng có các sắc độ khác nhau về độ sáng nên bạn có thể thay đổi độ sáng cho màu bằng cách *xoay vòng hue*

Để làm cho màu sáng hơn, hãy **xoay hue về phía hue sáng gần nhất - 60, 180, 300 độ**

<img width="360" src="https://user-images.githubusercontent.com/43769314/70025344-1a84f480-15e0-11ea-8e8f-ecc638ec2640.png">

Để làm cho màu tối hơn, hãy **xoay hue về phía hue tối gần nhất - 0, 120, 240 độ**

<img width="330" src="https://user-images.githubusercontent.com/43769314/70025395-47d1a280-15e0-11ea-9476-0d62b97f0dac.png">

Cách làm này khá hữu hiệu khi muốn tạo một pallete color cho màu sáng như màu vàng, khi đó các màu tối hơn sẽ có tông cam và tạo cảm giác ấm áp thay vì tạo ra cảm giác "tối tăm"

<img width="720" src="https://user-images.githubusercontent.com/43769314/70025993-e9a5bf00-15e1-11ea-89b8-cf52f5c0f048.png">

Dĩ nhiên, bạn cũng có thể kết hợp hai phương pháp trên, thay đổi hue và brightness

<img width="720" src="https://user-images.githubusercontent.com/43769314/70026345-e3fca900-15e2-11ea-8cc4-b6b1b1c68ef2.png">

Tuy nhiên đừng xoay hue quá 20-30 độ nếu không bạn sẽ có một màu khác hẳn so với màu ban đầu, thay vì một màu sáng hoặc tối hơn.

### Greys don’t have to be grey

Theo như định nghĩa, true grey có saturation là 0% - nó không có bất kì màu thực sự nào cả

<img width="580" src="https://user-images.githubusercontent.com/43769314/70027321-3939ba00-15e5-11ea-912a-0f1db92e3ed8.png">

Tuy nhiên trong thực tế, có rất nhiều màu tưởng chừng như grey nhưng thực ra có saturate khá mạnh

<img width="720" src="https://user-images.githubusercontent.com/43769314/70027687-0ba14080-15e6-11ea-92e1-3a06819cc18f.png">

Saturation làm cho grey có cảm giác nhẹ nhàng hoặc ấm áp riêng.

#### Color temperature

Tương tự như bóng đèn, những bóng đèn với ánh sáng vàng thường tạo cảm giác "ấm áp" hơn là bóng đèn với ánh sáng xanh

Tương tự như vậy, nếu bạn muốn làm cho grey nhẹ nhàng và "mát" hơn hãy saturate nó với một chút màu xanh

<img width="600" src="https://user-images.githubusercontent.com/43769314/70028156-39d35000-15e7-11ea-837f-a8ec1e842da8.png">

Nếu bạn muốn grey của bạn trông "ấm áp" hơn hãy saturate nó với một chút vàng, hoặc cam

<img width="600" src="https://user-images.githubusercontent.com/43769314/70031905-afdbb500-15ef-11ea-91ae-0e0aafcf7768.png">

### Accessible doesn’t have to mean ugly

Để đảm bảo cho thiết kế của bạn có thể được theo dõi một cách dễ dàng, normal text (dưới 18px) có độ tương phản: 4.5:1, text lớn hơn có độ tương phản ít nhất là 3:1

<img width="720" src="https://user-images.githubusercontent.com/43769314/70033085-18c42c80-15f2-11ea-925b-ba23fb4dd68b.png">

#### Flipping the contrast

Khi sử dụng chữ trắng cho background màu, bạn sẽ nhận ra mức độ cần thiết của độ tối của màu để đảm bảo tỉ lệ tương phản 4.5:1 

<img width="720" src="https://user-images.githubusercontent.com/43769314/70033261-70629800-15f2-11ea-8bb0-a3f943a3a234.png">

Tuy nhiên nếu sử dụng background tối màu, điều này sẽ khiến người dùng tập trung nhiều vào background thay vì nội dung text

<img width="720" src="https://user-images.githubusercontent.com/43769314/70033490-e5ce6880-15f2-11ea-8538-027c69301bde.png">

Bạn có thể giải quyết vấn đề này bằng cách đảo ngược sự tương phản, sử dụng chữ với màu đậm trên phông nền màu nhạt hơn.

<img width="720" src="https://user-images.githubusercontent.com/43769314/70033904-ba984900-15f3-11ea-87fc-ddffa8f2a3f4.png">

#### Rotating the hue

Trường hợp khó hơn text màu trắng trên background màu đó là cả text và background đều có màu, nếu chúng ta bắt đầu từ background color, sau đó chỉnh sửa saturation và lightness thứ chúng ta sẽ thu được là một màu text gần với màu trắng thuần khiết cũng như khó có thể đảm bảo tỉ lệ tương phản như đã nói ở trên

<img width="720" src="https://user-images.githubusercontent.com/43769314/70035731-cc2f2000-15f6-11ea-92b9-183ce5134b5a.png">

Bạn không muốn primary text và secondary text không có cùng màu, như đã biết có một số màu có độ sáng lớn hơn các màu còn lại, thay vì làm cho màu của bạn "trắng hơn", hãy xoay hue về hướng các màu sáng như yellow, cyan, magenta.

<img width="720" src="https://user-images.githubusercontent.com/43769314/70035898-157f6f80-15f7-11ea-9120-b19fc96d770b.png">

Điều này cũng giúp cho text dễ dàng quan sát hơn dù chúng có màu sắc đi chăng nữa.

### Don’t rely on color alone

Với những người dùng có thị giác màu kém, việc "dựa dẫm" vào màu quá nhiều không phải là một ý tưởng tốt. Như ví dụ dưới đây: những người dùng có thị giác màu kém, họ sẽ không biết card nào cho thấy trend tốt lên hay xấu đi.

<img width="720" src="https://user-images.githubusercontent.com/43769314/70105511-4e195a80-1684-11ea-9f48-c1798388f68f.png">

Cách giải quyết đơn giản ở đây đó là thêm các mũi tên lên xuống để thể hiện xu hướng của trend.

<img width="720" src="https://user-images.githubusercontent.com/43769314/70105579-920c5f80-1684-11ea-96df-efee655227a0.png">

Trong trường hợp của graph:

<img width="720" src="https://user-images.githubusercontent.com/43769314/70107040-bc601c00-1688-11ea-86e0-5193db70c58c.png">

Sử dụng những màu tương phản nhau, khi đó với người nhận thức màu kém việc phân biệt giữa light và dark color sẽ dễ dàng hơn phân biệt giữa các màu khác nhau

<img width="670" src="https://user-images.githubusercontent.com/43769314/70110947-14505000-1694-11ea-8fa1-429412b3c6ad.png">

## Creating Depth

### Emulate a light source

Thực tế, khi nhìn vào một số giao diện, bạn sẽ thấy có những phần nổi lên và ngược lại sẽ có những phần chìm xuống dưới background

<img width="700" src="https://user-images.githubusercontent.com/43769314/70111036-609b9000-1694-11ea-86e3-bbb60df95a1d.png">

Việc tạo ra hiệu ứng này có thể khá phức tạp nếu chỉ nhìn sơ qua, nhưng thực ra mọi chuyện hoàn toàn dễ dàng nếu bạn tuân thủ một quy luật cơ bản sau

#### Light comes from above

Hãy cùng nhìn vào cánh cửa phía dưới, mặc dù chỉ là flat image, nhưng chuáng ta vẫn cảm nhận được các phần panels của cánh cửa đang nổi lên, tại sao lại như vậy?

<img width="680" src="https://user-images.githubusercontent.com/43769314/70115840-4b2e6200-16a4-11ea-9135-256c5ae60153.png">

Cạnh phía trên của cánh cửa hướng về phía nguồn sáng và nhận nhiều ánh sáng hơn so với cạnh phía dưới

<img width="450" src="https://user-images.githubusercontent.com/43769314/70116974-939b4f00-16a7-11ea-898d-f1b895bd91e0.png">

Bây giờ hãy xem xét đến trường hợp của cabinet phía dưới:

<img width="670" src="https://user-images.githubusercontent.com/43769314/70117029-b463a480-16a7-11ea-854b-b7d4406aea9f.png">

Trong trường hợp này, panel sẽ có cảm giác "chìm xuống" do cạnh phía trên nhận ít ánh sáng hơn cạnh phía dưới.

<img width="430" src="https://user-images.githubusercontent.com/43769314/70117087-dfe68f00-16a7-11ea-929b-33c036b64ffa.png">

> Để tạo ra cảm giác tương tự cho thiết kế của bạn, hãy tiến hành mô phỏng lại hiệu ứng ánh sáng trong thực tế.

#### Simulating light in a user interface

Bản thân chúng ta cần hiểu rõ bản chất của component hay nói cách khác là *profile* của nó để từ đó đưa ra sự lựa chọn *chìm / nổi* phù hợp.

#### Raised elements

Người dùng thường có xu hướng nhìn theo hướng từ trên xuống dưới nên với 1 button thì cạnh trên sẽ sáng hơn cạnh dưới cũng như cần có bóng ở dưới do bị button "che khuất" từ phía trên (bóng này chỉ cần một độ dài ngắn là đủ)

<img width="690" src="https://user-images.githubusercontent.com/43769314/70967089-a3b82300-20d8-11ea-8314-b1796a6a60b3.png">

<img width="690" src="https://user-images.githubusercontent.com/43769314/70967114-b6325c80-20d8-11ea-8011-523d3859361d.png">

#### Inset elements

Là khi ta muốn các elements trông có vẻ lõm xuống, cạnh phía trên sẽ chắn sáng (sử dụng inset box shadow - với độ dài ngắn) và cạnh phía dưới sẽ nhận sáng (sử dụng bottom-border)

<img width="700" src="https://user-images.githubusercontent.com/43769314/70967784-b2073e80-20da-11ea-85a5-900442b18f5b.png">

<img width="680" src="https://user-images.githubusercontent.com/43769314/70967799-c0555a80-20da-11ea-8444-d5eeac540f81.png">

Cách xử lí hoàn toàn tương tự với các elements như input, checkbox

<img width="690" src="https://user-images.githubusercontent.com/43769314/70967831-dc58fc00-20da-11ea-8cc5-17f70537e935.png">

### Don’t get carried away

Trong thực tế, bạn hoàn toàn có thể vay mượn các thiết kế có sẵn về độ sâu do việc chỉnh sửa yếu tố này thường mất nhiều thời gian để có thể mô phỏng 1 cách chính xác giống như thực tế

## Use shadows to convey elevation

Sử dụng shadow cũng có thể tạo ra hiệu ứng xa gần cho elements tương ứng với trục ảo z

Với (small shadow, blur nhẹ) sẽ cho cảm giác element chỉ cao hơn "một chút" so với bề mặt giao diện, ngược lại với (large shadow, blur mạnh) sẽ cho cảm giác element gần với người dùng hơn

<img width="680" src="https://user-images.githubusercontent.com/43769314/70968836-af5a1880-20dd-11ea-8cd1-a2049694b9e9.png">

Những components gần với người dùng sẽ thu hút được sự chú ý của người dùng. Bạn cũng có thể sử dụng shadow với kích cỡ nhỏ (Small shadow) để tạo sự chú ý với người dùng nhưng vẫn đảm bảo không làm ảnh hưởng đến toàn bộ page.

<img width="690" src="https://user-images.githubusercontent.com/43769314/71052398-8ba2db00-218e-11ea-8709-ac86a0240249.png">

Medium shadow khá hữu dụng với dropdown, cũng như các phần tử cần có một vị trí gần người dùng hơn các phần tử khác.

<img width="690" src="https://user-images.githubusercontent.com/43769314/71052461-bb51e300-218e-11ea-8658-a048f42aa3bf.png">

Large shadow là một sự lựa chọn hoàn hảo đối với dialogs khi bạn muốn tập trung sự chú ý của người dùng vào element này

<img width="720" src="https://user-images.githubusercontent.com/43769314/71067454-e43a9e00-21b7-11ea-97da-89fe27eca48b.png">

#### Establishing an elevation system

Tương tự như với font, màu, space, ... việc thiết lập một hệ thống độ cao sẽ giúp đẩy nhanh tốc độ thiết kế cũng như đảm bảo tính thống nhất cho thiết kế của chúng ta.

Chỉ cần **5** shadow là vừa đủ.

Bắt đầu với shadow nhỏ nhất và lớn nhất, sau đó sẽ tiến hành hoàn thiện các shadow ở giữa theo thứ tự tăng dần tuyến tính về kích cỡ

<img width="680" src="https://user-images.githubusercontent.com/43769314/71067774-7e9ae180-21b8-11ea-95d4-b6974a40fc04.png">

#### Combining shadows with interaction

Shadow ngoài việc tạo cảm giác gần về thị giác cho người dùng, nó còn được sử dụng để cho thấy việc người dùng đang tương tác với item. Ví dụ như ở danh sách các items, item nào được chọn item đó sẽ có shadow, điều đó cho thấy người dùng *đang tương tác* với item đó, cũng như có thể *kéo* và *thả* nó, ...

<img width="660" src="https://user-images.githubusercontent.com/43769314/71068212-99ba2100-21b9-11ea-85a8-8f1fb92184a5.png">

Tương tự với hiệu ứng **press button**, shadow của button sẽ giảm khi được nhấn hoặc có thể bị loại bỏ

<img width="665" src="https://user-images.githubusercontent.com/43769314/71068624-73e14c00-21ba-11ea-90ae-29212f8ed38a.png">

> Đừng chỉ nghĩ về shadow, hãy nghĩ về vị trí của phần tử trên trục z và gán cho chúng một shadow thích hợp nhất

### Shadows can have two parts

Trong thực tế các shadows thường sẽ có 2 phần.
- Phần thứ nhất: lớn hơn, có chiều cao lớn hơn, blur lớn hơn, nó sẽ mô phỏng lại shadow đằng sau một object theo luồng sáng trực tiếp.

<img width="680" src="https://user-images.githubusercontent.com/43769314/71137588-17c70800-224c-11ea-9054-900060d2a737.png">

- Phần thứ hai: nhỏ hơn nhưng tối hơn, chiều cao ngắn hơn và blur nhỏ hơn, nó sẽ mô phỏng lại shadow ở phía dưới object, nơi mà các luồng sáng không hoặc khó có thể chạm tới.

<img width="670" src="https://user-images.githubusercontent.com/43769314/71137627-33caa980-224c-11ea-8459-83dc365ac4d9.png">

Trong thực tế nên kết hợp cả 2 loại shadows trên.

<img width="690" src="https://user-images.githubusercontent.com/43769314/71139593-f0733980-2251-11ea-9c5d-321b2c5340c3.png">

Khi các components tiến ra xa trang của chúng ta, loại shadow thứ 2 sẽ dần biến mất

<img width="700" src="https://user-images.githubusercontent.com/43769314/71139776-7abb9d80-2252-11ea-9091-b18be5e9079c.png">

### Even flat designs can have depth

Flat-design cũng được áp dụng các nguyên lí về độ sâu của thiết kế nhằm mô phỏng hiệu ứng ánh sáng trong thực tế.

#### Creating depth with color

> Các elements có màu sáng hơn sẽ cho cảm giác gần với người dùng hơn và ngược lại

<img width="690" src="https://user-images.githubusercontent.com/43769314/71139991-38df2700-2253-11ea-890f-0063a545debe.png">

#### Using solid shadows

Sử dụng shadow với độ cao ngắn và **không có blur** sẽ khiến cho component có cảm giác *nổi* hơn so với background nhưng cũng không làm mất đi *tính phẳng* của thiết kế

<img width="680" src="https://user-images.githubusercontent.com/43769314/71140250-0681f980-2254-11ea-987e-06b2d96efe6a.png">

### Overlap elements to create layers

Việc xếp chồng các elements cũng giúp cho thiết kế có cảm giác *đa tầng*

Ví dụ thay vì để card *lọt thỏm* giữa một background, hãy di chuyển card để nó nằm ở vùng chuyển giao giữa 2 background khác nhau, sẽ làm nổi trội tính *đa tầng* cho thiết kế

<img width="680" src="https://user-images.githubusercontent.com/43769314/71140399-7db78d80-2254-11ea-8b09-7b9668922a3d.png">

Bạn cũng có thể làm cho component có chiều cao lớn hơn parent của nó, qua đó khiến cho component trải (overlap) trên cả 2 backgrounds

<img width="670" src="https://user-images.githubusercontent.com/43769314/71143387-bf990180-225d-11ea-84ea-9d9ba141fe54.png">

Overlapping elements có thể áp dụng lên những components nhỏ hơn ví dụ như các controls trong carousel

<img width="675" src="https://user-images.githubusercontent.com/43769314/71143512-2a4a3d00-225e-11ea-97cd-3a436890b621.png">

#### Overlapping images

Kĩ thuật này có thể áp dụng cho images nhưng cũng có thể gây ra các xung đột về mặt màu sắc giữa các images

<img width="680" src="https://user-images.githubusercontent.com/43769314/71143786-1e12af80-225f-11ea-938b-29962e9c3172.png">

Để tránh điều này ta có thể thêm một "invisible border" xung quanh image - border này phải có màu giống với màu của background để qua đó tạo ra một khoảng không gian nhất định giữa các bức ảnh

<img width="685" src="https://user-images.githubusercontent.com/43769314/71143806-2c60cb80-225f-11ea-8e1c-3be022d75f85.png">

## Working with Images

### Use good photos

Hình ảnh cũng sẽ ảnh hưởng đến chất lượng của thiết kế kể cả khi những yếu tố khác có tốt như thế nào đi chăng nữa

<img width="680" src="https://user-images.githubusercontent.com/43769314/71152297-57581900-2279-11ea-8dd5-07b9f1f8211a.png">

### Text needs consistent contrast

Có những tình huống bạn cố thử nhiều màu sắc cho text trên một phông nền là một bức hình lớn nhưng đều thất bại. Như ví dụ dưới đây

<img width="685" src="https://user-images.githubusercontent.com/43769314/71790166-4fb6b380-3072-11ea-8e8a-9a7d60b9319c.png">

Thực ra nguyên nhân không nằm ở text mà nằm ở bức ảnh phông nền của bạn

#### The problem with background images

Một bức ảnh sẽ có cả những mảng sáng và mảng tối. Text màu trắng sẽ là một sự kết hợp tốt với mảng tối của ảnh và ngược lại. Tuy nhiên với các mảng sáng thì text màu trắng sẽ bị "chìm" thậm chí **không thể nhìn thấy được**.

<img width="675" src="https://user-images.githubusercontent.com/43769314/71790813-bb4e5000-3075-11ea-8551-754ddefbd7ab.png">

Để giải quyết vấn đề này, ta cần giảm đi tính "dynamic" của ảnh bằng cách giữ cho **độ tương phản** giữa text và ảnh ở mức thích hợp nhất có thể.

#### Add an overlay

Có một cách làm khá phổ biến, đó là "tráng" một lớp **semi-transparent overlay** lên trên image

<img width="680" src="https://user-images.githubusercontent.com/43769314/71792497-42062b80-307c-11ea-982b-d79b397a8c43.png">

Việc này sẽ làm giảm đi sức ảnh hưởng của độ tương phản mà background-image gây ra cho text

#### Lower the image contrast

Một cách làm khác ở đây là **làm giảm độ tương phản** và **tăng độ sáng** của background image qua đó sẽ làm giảm đi tính sáng tối vốn có của bức ảnh

<img width="720" src="https://user-images.githubusercontent.com/43769314/71954679-63584a80-3229-11ea-9885-2000367552a9.png">

#### Colorize the image

Một cách xử lí khác nữa là colorize cho bức ảnh của bạn. Bạn có thể sử dụng các phần mềm chỉnh sửa ảnh để có được một bức ảnh với màu tráng phù hợp, tuy nhiên nếu không sử dụng phần mềm nào cả, bạn có thể thực hiện như 3 bước dưới đây

1. **Giảm độ tương phản của bức ảnh**, để tạo ra sự cân bằng cho bức ảnh
2. **Bão hoà bức ảnh**, để loại bỏ các màu đang tồn tại
3. **Thêm solid fill**, sử dụng **multiply blend mode**

<img width="720" src="https://user-images.githubusercontent.com/43769314/71955793-a10aa280-322c-11ea-9cd9-5cd03e55e7ce.png">

Đây cũng là một cách để khiến cho background image của bạn hài hoà hơn với màu nhận diện của trang web

#### Add a text shadow

Nếu trong trường hợp bạn muốn bảo toàn những đặc trưng vốn có của background image, nhưng vẫn muốn đảm bảo độ tương phản cho text, text shadow sẽ là một sự lựa chọn tốt hơn cả. Tuy nhiên đừng biến nó trở thành box-shadow, do đó hãy sử dụng blur radius lớn hơn và **không thêm bất kì offset** nào khác

<img width="720" src="https://user-images.githubusercontent.com/43769314/71956491-aec12780-322e-11ea-87c0-58271ac4b0bc.png">

### Everything has an intended size

> Chúng ta đều biết, phóng to các bitmap images sẽ khiến cho chúng bị vỡ, và không giữ được độ sắc nét như ban đầu

<img width="650" src="https://user-images.githubusercontent.com/43769314/71956627-fcd62b00-322e-11ea-9daf-30fcafaf1d9c.png">

#### Don’t scale up icons

Ví dụ với một trang Landing Page, khi sử dụng icon cho phần "feature", bạn sẽ sử dụng SVG icon yêu thích của mình và đồng thời scale up nó cho đến khi nào vừa ý thì thôi. Vì là ảnh vector nên chất lượng không hề giảm khi ta scale up.

<img width="500" src="https://user-images.githubusercontent.com/43769314/71958885-bc79ab80-3234-11ea-8cea-5d4516d95ff3.png">

Đúng là về mặt chất lượng thì các SVG icons luôn đảm bảo nhưng việc scale up nó 3x, 4x so với kích cỡ ban đầu sẽ làm mất đi tính cân xứng vốn có của icon với intended size

<img width="500" src="https://user-images.githubusercontent.com/43769314/71959017-0f536300-3235-11ea-9da8-16212e8c0fbe.png">

Có một cách khác để "scale up" icon đó là bao lấy nó bởi 1 shape với background-color phù hợp

<img width="720" src="https://user-images.githubusercontent.com/43769314/71959216-82f57000-3235-11ea-9b46-25a66339e630.png">

Điều này khiến cho icon của bạn vừa đáp ứng yêu cầu về kích thước nhưng vấn giữ lại những đặc tính vốn có ở intended size

<img width="720" src="https://user-images.githubusercontent.com/43769314/71959281-b0421e00-3235-11ea-9393-eb1912ce926d.png">

#### Don’t scale down screenshots

Giả sử bạn muốn chèn một screenshoot về 1 feature nào đó vào landing page, tuy nhiên không gian lại quá hẹp khiến bạn phải thu nhỏ kích cỡ của screenshot xuống còn 70%. Điều này sẽ tạo ra cảm giác bạn đang **cố nhồi nhét nhiều thông tin, cũng như hình ảnh** vào một không gian hẹp, khiến cho người xem khá khó theo dõi.

<img width="720" src="https://user-images.githubusercontent.com/43769314/71961866-a4595a80-323b-11ea-921f-ee283d416d8e.png">

Font size thực tế là 16px, khi thu nhỏ sẽ có kích thước 4px, điều đó sẽ làm người dùng phải nheo mắt lại ở khoảng cách 2-inches để có thể xem được nội dung của screenshot

Giải pháp ở đây đó là chụp ảnh màn hình ở một layout nhỏ hơn (tablet chẳng hặn) cũng như chuẩn bị nhiều không gian nhất có thể cho screenshot trong landing page của bạn

<img width="700" src="https://user-images.githubusercontent.com/43769314/71962070-04500100-323c-11ea-8066-7926bb8212c0.png">

Hoặc bạn cũng có thể cân nhắc chỉ chụp screenshot ở những khu vực trung tâm của feature để có thể không cần scale down bức ảnh khi chỉ có một không gian hẹp cho nó

<img width="690" src="https://user-images.githubusercontent.com/43769314/71962186-4c6f2380-323c-11ea-8630-57020878b6e9.png">

Hoặc nếu bạn thực sự cần hình ảnh của toàn bộ app thì hãy tự tạo một version đơn giản cho nó, lược đi những chi tiết không cần thiết, thay những đoạn text bằng những đường kẻ màu đơn giản như dưới đây.

<img width="680" src="https://user-images.githubusercontent.com/43769314/71962474-d7e8b480-323c-11ea-931a-d23be6008dc3.png">

#### Don’t scale down icons, either

Tương tự như vậy, việc scale down 1 icon có thể khiến cho nó trở nên hỗn độn khi ta cố gắng "nhét" nhiều chi tiết vào một bức ảnh có kích cỡ nhỏ. Một ví dụ điển hình là **favicon** - các icons được sử dụng ở **page title của browser**

<img width="470" src="https://user-images.githubusercontent.com/43769314/72042818-d8438700-32f2-11ea-8af4-0390c6ffbf3a.png">

Cách tiếp cận tốt hơn đó là **vẽ lại** một phiên bản đơn giản hơn của icon đó với kích thước mà chúng ta mong muốn thay vì phó mặc điều đó cho browser

<img width="570" src="https://user-images.githubusercontent.com/43769314/72042842-eabdc080-32f2-11ea-9d5f-40ee1afa9e5c.png">

### Beware user-uploaded content

Nếu trang web của bạn phụ thuộc vào nội dung (hình ảnh) mà người dùng tải lên, hãy chú ý rằng

> Đừng để chúng ảnh hưởng đến thiết kế của bạn

#### Control the shape and size

Giữ nguyên tỉ lệ chiều dài, rộng của ảnh khi hiển thị có thể **phá vỡ** cấu trúc layout của bạn

<img width="685" src="https://user-images.githubusercontent.com/43769314/72043177-d4fccb00-32f3-11ea-96fc-62910b422a4c.png">

Thay vì để cho người dùng tự ý phá vỡ cấu trúc của bạn, hãy đặt các ảnh được tải lên bởi người dùng vào vị trí trung tâm trung một container cố định và loại bỏ đi những thành phần thừa thãi của bức ảnh đó

<img width="720" src="https://user-images.githubusercontent.com/43769314/72043433-74ba5900-32f4-11ea-9a18-8664756f1e40.png">

Khá dễ dàng để có được điều này bằng cách thiết lập thuộc tính **background-size** trong CSS với giá trị **cover**

#### Prevent background bleed

Khi ảnh của người dùng có background color trùng với background color của UI, ảnh của người dùng sẽ bị mất đi kích thước vốn có của nó (hiện tượng **bleed**)

<img width="720" src="https://user-images.githubusercontent.com/43769314/72044344-e72c3880-32f6-11ea-8c61-6c8b195f7282.png">

Thay vì giải quyết vấn đề này bằng cách thêm một border, hãy sử dụng **inner box shadow nhẹ** cho ảnh của người dùng

<img width="720" src="https://user-images.githubusercontent.com/43769314/72044553-59048200-32f7-11ea-89ed-11c1af114223.png">

Border có thể gây ra xung đột về màu sắc cho ảnh, trong khi hiếm có người dùng nào lại có thể nhận ra được sự xuất hiện của inner box shadow

Một giải pháp khác đó là sử dụng semi-transparent inner border

<img width="665" src="https://user-images.githubusercontent.com/43769314/72044983-77b74880-32f8-11ea-9d88-7a9e2e095c3d.png">

## Finishing Touches

### Supercharge the defaults

Không phải việc thêm những chi tiết mới cho thiết kế cũng là một ý hay, thay vào đó hãy tận dụng tối đa những gì đang có cho thiết kế của bạn

Ví dụ: Với 1 danh sách (bullet list) thay vì sử dụng bullet bạn có thể sử dụng các icon

<img width="720" src="https://user-images.githubusercontent.com/43769314/72045980-c665e200-32fa-11ea-85db-a7cf31f15164.png">

Checkmark và mũi tên làn những lựa chọn phổ biến cho thiết kế, tuy nhiên với các danh sách có liên quan đến bảo mật, sử dụng các icon móc khoá sẽ là một ý tưởng độc đáo

<img width="720" src="https://user-images.githubusercontent.com/43769314/72046169-2c526980-32fb-11ea-8389-671a49a6e6ac.png">

Tương tự với những câu quote với mục đích quảng bá - bằng cách tăng font size và thay đổi màu

<img width="720" src="https://user-images.githubusercontent.com/43769314/72050581-d387ce80-3304-11ea-8bbe-42e0080d954e.png">





