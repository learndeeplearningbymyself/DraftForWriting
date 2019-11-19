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

#### Developing your intuition

