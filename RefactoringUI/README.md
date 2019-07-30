### Deciding what you actually want

Đôi khi việc tham khảo từ những sites tương tự sẽ có ích khá nhiều. Nếu những trang tương tự như ý tưởng của bạn hướng đến **business** hay **sự thân thiện** thì bạn cũng nên làm tương tự.

Tuy nhiên việc vay mượn ý tưởng thiết kế quá nhiều sẽ khiến cho thiết kế của bạn trở thành **sản phẩm hạng hai**.

## Limit your choices

Khi có quá nhiều lựa chọn cho fonts chữ cũng như màu sắc sẽ khiến việc quyết định thiết kế trở nên khó khăn. Ví dụ như:

- Nên để opacity là 10% hay 15% ?
- margin-bottom của button nên là 18px hay 20px ?
- Chiều cao của avatar nên là 24px hay 25px
- ...

Vậy chúng ta có thể đưa ra quyết định như thế nào về thiết kế cuối cùng khi không có gì trong số chúng là quá tồi ?

### Define systems in advance

Thay vì chọn các giá trị như kích cỡ font, màu sắc từ một thư viện vô tận các yếu tố đó, chúng ta nên *xây dựng một hệ thống cơ bản cho thiết kế của mình* và bắt đầu thiết kế từ đó

- Đừng tìm kiếm những màu mới khi thiết kế UI mới, thay vào đó hãy lựa chọn một hệ thống màu cơ bản cho thiết kế của mình ngay từ đầu (8 - 10 màu)

<img src="https://user-images.githubusercontent.com/43769314/62095587-d8f3de00-b2bb-11e9-9cd6-f45626cac2fb.png" width="720">

- Đừng chỉnh từng pixel một cho đến khi font chữ trở nên hoàn hảo mà hãy tự thiết kế cho mình một hệ thống font size cụ thể ngay từ đầu

<img src="https://user-images.githubusercontent.com/43769314/62095614-e9a45400-b2bb-11e9-8780-a4cdd54215b0.png" width="720">

Làm những việc như thế này có thể khiến bạn khá vất vả ngay từ đầu nhưng mỗi khi thêm một UI mới thì việc lựa chọn màu sắc, font chữ, ... lại không quá khó khăn và sẽ giúp bạn tiết kiệm rất nhiều thời gian cho việc thiết kế.

### Designing by process of elimination

Khi tiến hành thiết kế dựa theo một tập các giá trị ràng buộc giới hạn sẽ dễ dàng hơn việc thiết kế với nhiều *sự lựa chọn đúng đắn*

Lấy ví dụ khi thiết kế icon cho app. Ta lựa chọn tập giá trị kích cỡ icon là: 12px, 16px, 24px, 32px. Chọn một kích cỡ cho ta *cảm giác* là tốt nhất (ví dụ 16px), so sánh kích cỡ này với 2 kích cỡ khác là 24px, 12px.

Nếu giá trị 16px này ổn thì mọi việc đã OK. Nếu ngược lại ta sẽ lấy giá trị mới này làm "trung tâm" rồi đem đi so sánh với các giá trị khác đến khi nào *thấy ổn* thì thôi.

Cách tiếp cận này có thể áp dụng cho bất kì yếu tố nào trong thiết kế miễn sao bạn định nghĩa sẵn một hệ thống các giá tri cho chúng.

### Systematize everything

Càng định nghĩa trước nhiều hệ thống thì việc thiết kế sẽ trở nên dễ dàng hơn rất nhiều. Dưới đây là danh sách một vài hệ thống mà chúng ta nên thiết kế trước

- Font size
- Font weight
- Color
- Border radius
- Margin
- Padding

Chúng ta không nhất thiết phải thiết lập toàn bộ các hệ thống ngay từ đầu nhưng việc giữ mindset theo cách tiếp cận này là vô cùng quan trọng. Luôn tìm kiếm cơ hội đưa ra các hệ thống mới mỗi khi đưa ra các quyết định thiết kế mới

# Hierarchy is Everything

## Not all elements are equal

Nếu bạn vẫn nghĩ thiết kế là tạo ra một thứ gì đó *nhìn được* thì bạn đã lầm. Việc thiết kế không chỉ đơn thuần là làm **style một cách hời hợt** như vậy

Ta có một khái niệm đó là *Visual Hierarchy* để chỉ việc các thành phần trong UI cũng cần có liên hệ với nhau.

Nếu các thành phần trong thiết kế không có liên hệ gì với nhau, có thể chúng sẽ *cạnh tranh* nhau khiến cho thiết kế trông khá *hài hước* và đặc biệt là **không tạo ra được sự thống nhất** trong thiết kế, nó giống như một bức tường lớn với các nội dung đối lập và cuối cùng chẳng truyền đạt được bất cứ một thông điệp gì cả

Ảnh phía dưới là một hệ thống không có sự phân cấp, kế thừa, nhấn mạnh tính chính phụ của thông tin

<img src="https://user-images.githubusercontent.com/43769314/62106177-862c1d80-b2df-11e9-9ee3-62b3d5fc0875.png" width="720">

Ảnh phía dưới là hệ thống đã có sự phân cấp thông tin chính, phụ, qua đó khiến việc nắm bắt thông tin dễ dàng hơn rất nhiều (dù font chữ, tông màu không thay đổi gì cả)

<img src="https://user-images.githubusercontent.com/43769314/62106272-cf7c6d00-b2df-11e9-9794-da144d8edb41.png" width="720">

## Size isn’t everything

Không nên chỉ dựa hoàn toàn vào font size. Trong khi có nhiều yếu tố khác như:
- Màu sắc
- Font weight

Cũng ảnh hưởng không kém đến hệ thống phân cấp kế thừa trong thiết kế, thay vì giữ nguyên quan điểm

> primary content sẽ có font size lớn, secondary content sẽ có font size nhỏ

Ví dụ: Nếu có 4, 5 cấp trong hệ thống phân cấp thông tin thì ta sẽ phải sử dụng 4, 5 font size -> điều này là khá bất hợp lí vì trong 1 site chỉ nên sử dụng **tối đa 3 font sizes** mà thôi

Với các text hỗ trợ, cấp thấp ta có thể sử dụng những **màu nhạt hơn** hoặc với những nội dung quan trọng như tiêu đề bài viết thì ta sẽ **làm đậm** nó lên. Ngoài ra việc sử dụng quá nhiều cỡ chữ có thể ảnh hưởng đến tính dễ đọc (readability) của thiết kế

Trong 1 site chỉ nên:

- Sử dụng 2 hoặc 3 màu
  - Dark color cho primary content (tiêu đề article)
  - Grey color cho secondary content (như ngày mà article được đăng)
  - Lighter grey cho nội dung cấp 3 (copyright notice trong footer)

- Tương tự chỉ cần 2 font weights là đủ
  - 400, 500 (normal font weight) cho các text thông thường
  - 600, 700 (heavier font weight) cho các nội dung muốn nhấn mạnh

<img src="https://user-images.githubusercontent.com/43769314/62119405-7110b800-b2fa-11e9-8314-baa62ee86753.png" width="720">
