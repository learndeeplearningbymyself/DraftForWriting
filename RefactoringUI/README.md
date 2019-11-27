### Don’t shrink an element until you need to

Giả sử bạn đang thiết kế một login card. Với full screen bạn chọn **6 column** cho login card và 6 column trống 2 bên (mỗi bên 3 column). Nhưng khi kích cỡ màn hình thu nhỏ lại thì login card cũng sẽ nhỏ lại theo, vậy bạn cần chỉnh lại cho login card lên **8 column**

<img src="https://user-images.githubusercontent.com/43769314/62682025-13fdbc00-b9f6-11e9-9106-ed516b7e01fb.png" width="720">

Vì sẽ có 1 khoảng các **screen-sizes** mà kích cỡ của login card sẽ nhỏ đi khi kích cỡ màn hình rộng ra

Do trong grid-system, chiều rộng có giá trị dynamic. Nên thay vì quá phụ thuộc vào grid, ta se định nghĩa **max-width** mà chỉ **force shrink** khi kích cỡ màn hình nhỏ hơn **max-width** mà thôi

<img src="https://user-images.githubusercontent.com/43769314/62682052-2677f580-b9f6-11e9-8f88-ee393bdd970f.png" width="720">

## Relative sizing doesn’t scale

Giả sử ta đang thiết kế một trang article cho một màn hình cỡ lớn (desktop). Body font size sẽ là 18px, trong khi title font size là 45px. Về cơ bản sự tương quan về kích cỡ này là khá hợp lí cho màn hình desktop.

Vậy công thức rút ra ở đây là 

> Title font size = Body font size * 2.5

Định nghĩa tương quan kích thước kiểu này gọi là **relative relationship**
Nhưng liệu điều này có phù hợp khi kích cỡ màn hình nhỏ đi hay không?

Nếu gấp 2.5 thì ta có thể coi **Title font size** bằng **2.5em**. (Về đơn vị **em** tham khảo [ở đây](https://github.com/learndeeplearningbymyself/TIL/issues/1]))


Với màn hình có kích cỡ nhỏ, để đảm bảo line length ta sẽ cho body font size có kích cỡ 14px, nếu giữ tỉ lệ kích cỡ trên thì kích cỡ của title sẽ là 35px trông sẽ như dưới đây

<img src="https://user-images.githubusercontent.com/43769314/62684281-4e1d8c80-b9fb-11e9-9c24-be924914df0c.png" width="720">

Tuy nhiên thay vì áp dụng cứng nhắc tỉ lệ này, ta sẽ chỉnh cho title có kích cỡ 24px thì sẽ trông như dưới đây

<img src="https://user-images.githubusercontent.com/43769314/62684433-a94f7f00-b9fb-11e9-8197-f75f1abc03c6.png" width="720">

Rõ ràng việc chỉnh font size cho title nhỏ đi trông sẽ phù hợp hơn cho màn hình có kích cỡ nhỏ, và ở đây ta có tỉ lệ là 1.5-1.7

Qua đó ta có thể rút ra kết luận là **relative relationship** không hệ tồn tại và cũng không có lợi ích gì khi thử nó với nhiều kích cỡ màn hình khác nhau

Như một luật tổng quát ta có

> Các phần tử có kích cỡ lớn trên màn hình lớn sẽ bị thu nhỏ nhanh hơn là các phần tử có kích cỡ nhỏ khi kích cỡ màn hình bị thu nhỏ. Không có sự khác biệt quá nhiều giữa phần tử lớn và nhỏ ở màn hình có kích cỡ nhỏ

### Relationships within elements

Tương tự như vậy trong cùng một element cũng không nên dựa theo 1 tỉ lệ cứng nhắc nào đó

Ví dụ như việc scale up, down button. Với màn hình to, button có (font-size: 20px, padding: 15px 20px) - nếu giữ nguyên tỉ lệ padding top-down = font-size thì sẽ trông như sau

<img src="https://user-images.githubusercontent.com/43769314/62686010-ca659f00-b9fe-11e9-8da0-8f24856ce178.png" width="720">

Tuy nhiên nếu thay đổi các kích cỡ này một cách không quá cứng nhắc thì sẽ như sau

<img src="https://user-images.githubusercontent.com/43769314/62686530-e1f15780-b9ff-11e9-8966-44f4fe6915a7.png" width="720">

Rõ ràng ảnh phía dưới cho ta cảm giác nút nhỏ thật sự *nhỏ*, nút lớn thực sự *lớn*

Vậy nên hãy từ bỏ thói quen scale mọi thứ thật *cân xứng*, hãy làm mọi thứ độc lập với nhau, điều đó sẽ khiến bạn cảm thấy tự do hơn khi thay đổi kích thước các elements

## Avoid ambiguous spacing

Khi thiết kế **background color**, **spacing** cũng như các **seperators** là công cụ để phân biệt giữa các *elements groups* với nhau

Thiếu đi chúng các elements trong cùng 1 group sẽ thiếu đi sự liên kết
Như ví dụ dưới đây, margin giữa label với input là như nhau nên không có sự liên kết giữa label và input trong cùng 1 group

<img src="https://user-images.githubusercontent.com/43769314/62750787-5083f300-ba9c-11e9-9663-90f46b2bf698.png" width="720">

Nếu thay đổi khoảng cách giữa input với label phía dưới nó, thì sẽ trông như thế này

<img src="https://user-images.githubusercontent.com/43769314/62750798-5bd71e80-ba9c-11e9-993c-1660df3e01ea.png"" width="720">

Rõ ràng ở hình thứ 2, mọi thứ đã có sự liên kết rõ ràng hơn

Cũng tương tự như khi thiết kế article (**khoảng cách phía trên section heading** là không đủ lớn) hoặc trong **bulleted list**, khi mà khoảng cách giữa các **bulleted** bằng với **line-height** của 1 bullet.

<img src="https://user-images.githubusercontent.com/43769314/62750960-df910b00-ba9c-11e9-9b57-30464b3cc6ae.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/62750974-eddf2700-ba9c-11e9-8ea7-9975bcd4366d.png" width="720">

Điều tương tự cũng có thể xảy ra với các phần tử nằm ngang

<img src="https://user-images.githubusercontent.com/43769314/62751024-2bdc4b00-ba9d-11e9-96c7-06e67e202770.png" width="720">

Bất cứ khi nào bạn muốn dựa theo khoảng cách để kết nối các phần tử thì hãy ghi nhớ rằng

> Khoảng cách xung quanh group elements luôn phải lớn hơn khoảng cách bên trong group

> Một UI tồi là khi nó quá khó để hiểu

# Designing Text

## Establish a type scale

Trong thực tế, không quá khó để tìm thấy một thiết kế có quá nhiều font-size

<img src="https://user-images.githubusercontent.com/43769314/62755913-c7c38200-bab0-11e9-85c3-ae72c85dd55d.png" width="720">

Chọn lựa font-size mà thiếu đi tính hệ thống có thể là 1 ý tưởng tồi với 2 lí do như sau
1. Khiến cho giao diện trở nên thiếu đi tính thống nhất
2. Làm giảm tiến độ công việc

### Choosing a scale

#### Modular scales

Một cách tiếp cận đó là tính toán dựa theo **tỉ lệ**
- 4:5 - *major third*
- 2:3 - *perfect fifth*
- 1:1.618 - *golden ratio*

Cách tiếp cận này thường gọi là **modular scale**. Có thể chọn **base font size** là 16px vì *đây là kích cỡ font mặc định của mọi trình duyệt*

Cách tiếp cận này trong thực tế lại không hợp lí vì 2 lí do
1. **Chúng ta thường có kết quả dưới dạng phân số**
2. **Thực tế, chúng ta cần nhiều font size hơn**
  - Việc sử dụng cách tính toán trên chỉ thích hợp với **article design** với **interface design** đôi khi chúng ta muốn các cỡ font nằm giữa khoảng **12px- 16px** hoặc **16px - 21px**
  - Để giải quyết vấn đề, có thể nghĩ tới giải pháp với tỉ lệ 8:9. Tuy nhiên đây thực ra lại là **chọn cỡ font mà ta mong muốn một cách tuỳ ý**

#### Hand-crafted scales

Một cách tiếp cận thường dùng trong thực tế đó là **dùng tay**. Thật vậy, việc tự tạo **bằng tay** một hệ thống sẽ giúp bạn chủ động hơn trong việc kiểm soát các kích cỡ hiện có thay vì phó mặc mọi thứ cho một hệ thống tính toán

Dưới đây là một ví dụ về một hệ thống scale được sử dụng rất nhiều trong thực tế

<img src="https://user-images.githubusercontent.com/43769314/62756782-01e25300-bab4-11e9-87e2-74bc70b0e80b.png" width="720">

<img src="https://user-images.githubusercontent.com/43769314/62756835-25a59900-bab4-11e9-9897-3edfd7dd70dc.png" width="720">

#### Avoid em units

Không nên sử dụng đơn vị em, vì nó là giá trị mang tính chất tương đối. Giá trị em của **nested elements** phụ thuộc vào giá trị của element cha (relative value), từ đó dẫn đến tình trạng tạo ra các giá trị mà ta không hề mong muốn cho font chữ

<img src="https://user-images.githubusercontent.com/43769314/66882296-d5433e00-f004-11e9-877e-ebfa5f6b8ca4.png" width="720">

Như ví dụ trên, nếu một phần tử có font size là 1.25em (mặc định là 20px) thì phần tử con của nó (nếu có giá trị font size là 1em) thì lúc này giá trị thực (theo đơn vị px) sẽ là 20px thay vì 16px như mong muốn

> Hãy sử dụng px hoặc rem nếu bạn muốn bảo toàn những gì đang xây dựng cho giao diện của mình

### Use good fonts

Dưới đây là một vài tricks để có thể chọn ra fonts (typefaces) phù hợp cho UI của bạn

#### Play it safe

Nếu đang phân vân thì **san-serif** luôn là một lựa chọn an toàn - VD như **Helvetica**

Còn nếu bạn không tin tưởng vào sự cảm nhận của bản thân thì hãy sử dụng **system font stack** như sau:

1. -apple-system
2. Segoe UI
3. Roboto
4. Noto Sans
5. Ubuntu
6. Cantarell
7. Helvetica Neue

Có thể đó không phải là những sự lựa chọn tốt nhất nhưng ít nhất, người dùng cũng có thể đọc nó một cách dễ dàng

#### Ignore typefaces with less than five weights

Điều này có thể không hoàn không đúng nhưng các fonts có số lượng weights nhiều thường được tạo ra với một sự cẩn thận và chi tiết nhiều hơn so với các fonts có ít weights.

Trên Google fonts, filter "number of styles" là sự kết hợp của các weights hiện có cũng như các mẫu italic khác của các weights tương ứng

#### Optimize for legibility

Các Font sử dụng cho headline thương có khoảng cách giữa các chữ hẹp và kí tự lowercase với chiều cao thấp hơn so với fonts cho các sizes chữ nhỏ hơn.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69127093-f3f99080-0aec-11ea-85b9-4ca4af92eeb6.png">

Hãy luôn ghi nhớ điều này để tránh việc sử dụng fonts với x-height bé cho main UI text

#### Trust the wisdom of the crowd

Nếu một font là phổ biến thì chứng tỏ font đó là khá tốt, có nhiều font directories cho phép chúng ta có thể chọn fonts dựa theo mức độ phổ biến (popularity), đây là một điều tuyệt vời khi chúng ta cần chọn các fonts có cá tính (khác hẳn với các font trung tính)

<img width="720" src="https://user-images.githubusercontent.com/43769314/69127501-b0535680-0aed-11ea-9ca8-05bc75aa8f88.png">

#### Steal from people who care

Lựa chọn 1 site mà bạn yêu thích, inspect để biết được site đó sử dụng font nào. Họ thường sẽ chọn được các fonts khá tuyệt mà bằng cách tiếp cận "an toàn" thông thường, bạn có thể sẽ không tìm được.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69127881-7df62900-0aee-11ea-865f-c823f7f2b649.png">

### Keep your line length in check

Khi tiến hành styling cho paragraph, chúng ta thường dễ mắc lỗi thiết kế (fitting the text to the layout) khiến cho đoạn text dài và khó đọc (ảnh hưởng xấu đến trải nghiệm đọc của người dùng)

<img width="720" src="https://user-images.githubusercontent.com/43769314/69203042-b2b5bf00-0b86-11ea-8298-284919f39ec9.png">

Để tạo ra trải nghiệm đọc tốt nhất, hãy đảm bảo các paragraphs của bạn có chiều rộng nằm trong khoảng **45-75 kí tự mỗi dòng**. Cách thiết lập dễ dàng nhất ở đây là sử dụng đơn vị *em* - có tính tương đối với font size hiện tại. Chiều rộng trong khoảng **20-35em** là thích hợp nhất.

#### Dealing with wider content

Nếu bạn đang tiến hành kết hợp giữa paragraph với ảnh hoặc các components lớn khác, bạn vẫn nên chú ý giới hạn chiều rộng của paragraph kể cả khi khu vực nội dung chính cần phải rộng hơn để chứa thêm các elements khác.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69395990-38bb3c80-0d24-11ea-9c91-44a8a5c55003.png">

<img width="720" src="https://user-images.githubusercontent.com/43769314/69396015-47095880-0d24-11ea-932a-980fdb40380a.png">

Thoạt qua ta thấy có vẻ như cách làm thứ hai sẽ phản trực giác khi sử dụng nhiều kích cỡ chiều rộng khác nhau trong cùng một vùng nội dung nhưng kết quả là giao diện của chúng ta sẽ trở nên thoáng hơn rất nhiều.

### Baseline, not center

Sẽ có những trường hợp, bạn phải kết hợp sử dụng nhiều loại font sizes khác nhau trong cùng một dòng (VD: như đối với dòng tiêu đề của 1 card: tên card, các action names - theo thứ tự từ trái sang phải)

Thông thường ở trường hợp này bạn sẽ nghĩ ngay đến giải pháp căn lề dọc các nội dung với font sizes khác nhau. Đó không hẳn là một ý tưởng tồi, tuy nhiên điều đó chỉ thích hợp khi bạn có thể tạo được một khoảng không gian trống giữa các cỡ chữ khác nhau như hình dưới đây:

<img width="720" src="https://user-images.githubusercontent.com/43769314/69507719-cee6a100-0f76-11ea-9b6e-474afdeab8b4.png">

Tuy nhiên khi không có đủ khoảng cách, mọi thứ trông thật là vụng về:

<img width="720" src="https://user-images.githubusercontent.com/43769314/69507770-ff2e3f80-0f76-11ea-8e7d-fa17fa0817ee.png">

Một cách tiếp cận tốt hơn cho việc sử dụng nhiều font sizes trong một dòng đó chính là *baseline* của chúng - đây là đường kẻ ngang tưởng tượng, có vai trò như chân đế của các chữ cái

<img width="720" src="https://user-images.githubusercontent.com/43769314/69508020-e5d9c300-0f77-11ea-812c-ce6d61ecbc7b.png">

Khi sử dụng *baseline* cho nhiều font sizes khác nhau, bạn đang tận dụng khá tốt yếu tố căn gióng mà bản thân đôi mắt của bạn có thể cảm nhận được

<img width="720" src="https://user-images.githubusercontent.com/43769314/69508196-6d273680-0f78-11ea-8372-90be8a761c6a.png">

Trông dễ nhìn và "thoáng hơn" rất nhiều.

### Line-height is proportional

Line-height 1.5 là một điểm khởi đầu tốt cho tính dễ đọc của văn bản, việc chọn line-height phù hợp cho nội dung văn bản thường khá phức tạp hơn so với sử dụng cùng một giá trị cho mọi trường hợp

<img width="720" src="https://user-images.githubusercontent.com/43769314/69509138-3272cd80-0f7b-11ea-9f60-c4ad746aa97f.png">

#### Accounting for line length

Việc thêm khoảng cách giữa các dòng khiến cho người đọc không bị rối mắt, qua đó tránh được trường hợp một dòng vị đọc 2 lần, ... Nguyên nhân là do line-height quá ngắn. Khi line-height ngắn thì người đọc sẽ dễ dàng quay trở lại lề trái của dòng vừa đọc xong do người đọc không chắc chắn được về dòng tiếp theo họ cần phải đọc.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69511391-3dc9f700-0f83-11ea-93db-a7fbf784c206.png">

Vấn đề sẽ trở nên nghiêm trọng hơn khi các dòng text qúa dài, khi mắt người đọc phải đánh ra càng xa (theo chiều ngang) thì họ càng dễ mất định hướng về điểm neo của dòng tiếp theo. Điều đó có nghĩa rằng line-height và chiều rộng của paragraph cần phải tỉ lệ thuận, với nội dung có chiều rộng hẹp nên sử dụng **line-height: 1,5**, với nội dung có chiều rộng lớn nên sử dụng **line-height: 2**

<img width="720" src="https://user-images.githubusercontent.com/43769314/69515372-be8fef80-0f91-11ea-99ef-e9644450c262.png">

#### Accounting for font size

Ngoài chiều rộng của dòng thì font size cũng là yếu tố ảnh hưởng đến việc lựa chọn line-height. Với các font sizes nhỏ ta cần khoảng cách giữa các dòng để người đọc có thể dễ dàng tìm được dòng tiếp theo khi kết thúc dòng đang đọc

<img width="720" src="https://user-images.githubusercontent.com/43769314/69518580-49291c80-0f9b-11ea-907a-769c4725db4b.png">

Tuy nhiên với text cỡ lớn không cần quá nhiều line-spacing, lúc này chỉ cần **line-height = 1** là đủ

<img width="720" src="https://user-images.githubusercontent.com/43769314/69520419-03bb1e00-0fa0-11ea-8717-c90c986fdd42.png">

> Line-height và font size tỉ lệ nghịch với nhau - sử dụng line-height cao hơn cho chữ nhỏ và line-height thấp hơn cho chữ to

### Not every link needs a color

Thông thường với các links có trong 1 đoạn văn, chúng thường được làm nổi để thể hiện rằng "đây là một link".
Tuy nhiên khi xử lí các giao diện chỉ có links thì việc làm nổi này đôi khi lại tạo ra một sự gượng ép không cần thiết, khiến giao diện sẽ trở nên khó nhìn hơn.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69525059-a4aed680-0faa-11ea-8f34-c51ac5153171.png">

Thay vào đó có thể sử dụng cách nhấn mạnh "nhẹ nhàng hơn" thông qua việc, sử dụng font weight đậm hơn cũng như màu chữ tối hơn

<img width="720" src="https://user-images.githubusercontent.com/43769314/69525189-e9d30880-0faa-11ea-9b78-17add451e9f0.png">

Tuy nhiên có những links không cần thiết phải nhấn mạnh vì chúng không phải là phần chính trong giao diện, cũng như được người dùng click vào nhiều, khi đó ta có thể thêm **underline** hoặc **thay đổi màu** *chỉ khi người dùng hover* lên links.

<img width="720" src="https://user-images.githubusercontent.com/43769314/69595410-cb205080-1042-11ea-8520-b045bb435aa5.png">

Nó vẫn đủ để người dùng có thể nhận ra rằng đây là link nhưng lại không tạo ra sự cạnh tranh về tính chú ý đối với các phần quan trọng khác trên trang.

### Align with readability in mind

Căn lề text dựa theo thứ tự viết của ngôn ngữ (thường là từ trái sang)

<img width="720" src="https://user-images.githubusercontent.com/43769314/69607199-1567f880-1068-11ea-9bdf-ba6c26312f80.png">

#### Don’t center long form text

Căn lề giữa trông khá tuyệt với headlines hoặc các đoạn text ngắn, cũng như các text blocks độc lập

<img width="720" src="https://user-images.githubusercontent.com/15076665/69639107-529bad00-109f-11ea-9f44-c3b9b4b43948.png">

Tuy nhiên nếu phần nào đó dài hơn 2 hoặc 3 dòng thì ta nên căn trái

<img width="720" src="https://user-images.githubusercontent.com/15076665/69639202-7828b680-109f-11ea-92f6-04272e53ea19.png">

Nếu bạn có 1 text block có độ dài lớn hơn các text blocks còn lại, cách sửa tốt nhất là làm "ngắn nó" để qua đó tạo ra sự thống nhất cho giao diện.

<img width="720" src="https://user-images.githubusercontent.com/15076665/69639410-cf2e8b80-109f-11ea-9a90-8106505d1697.png">

#### Right-align numbers

Với các bảng có chứa số liệu, ta nên căn phải để có thể so sánh nhanh nhất có thể

<img width="720" src="https://user-images.githubusercontent.com/15076665/69639864-b2468800-10a0-11ea-801f-e785110cd605.png">

#### Hyphenate justified text

Jusitified text trông khá ổn với các trang web tuy nhiên trong một số trường hợp đặc biệt, nó có thể tạo ra những khoảng trông bất thường giữa các từ với nhau

Những trường hợp đó, ta nên sử dụng "-" - dấu gạch nối như một giải pháp

<img width="720" src="https://user-images.githubusercontent.com/15076665/69640216-56303380-10a1-11ea-9f02-022d9b666041.png">

<img width="720" src="https://user-images.githubusercontent.com/15076665/69640246-634d2280-10a1-11ea-853d-91fa680f8e13.png">

### Use letter-spacing effectively

Thông thường chúng ta sẽ follow theo thiết kế của font chữ chứ không cần phải để ý đến **letter-spacing**

<img width="720" src="https://user-images.githubusercontent.com/43769314/69697126-0c892c80-1125-11ea-97a0-27b354927783.png">

#### Tightening headlines

> Phân biệt nhanh giữa Typeface và Font. Typeface: Arial, Font (Arial: cỡ chữ 14, Arial: cỡ chữ 15, Arial: loại in nghiêng (italic)

Một font family được thiết kế với các letter-spacing phù hợp 
