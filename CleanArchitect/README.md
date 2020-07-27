# Clean Architect

※ Mọi hình ảnh trong bài dịch đều được lấy từ sách 「Clean Architecture 達人に学ぶソフトウェアの構造と設計」

## Part 1: Introduction
### Chapter 1: Design and Architecture

#### Mục tiêu 

Software design (cũng có thể gọi là Software architect) có thể chia thành 2 phần:
- Thành phần "level thấp"
- Thành phần "level cao"

Mục tiêu của Software architect là:
- Tạo ra một hệ thống như mong muốn
- Giảm tối đa chi phí bảo trì

Thiết kế tốt: đảm bảo yêu cầu từ khách hàng, giảm tối đa chi phí
Thiết kế tồi: tốn nhiều chi phí bảo trì

#### Case study

Xét một ví dụ như sau: sau mỗi lần relase, số nhân sự cho team kĩ thuật lại tăng (như biểu đồ 1-1 bên dưới) , liệu đây có là một tín hiệu tích cực ?

<img src="https://user-images.githubusercontent.com/43769314/88498430-0aea6e00-cffe-11ea-9388-7299a0620383.png" width="720">

*Biểu đồ 1-1*

NHƯNG ở biểu đồ 1-2 dưới đây, số lượng những dòng code mới dường như đã chạm tới ngưỡng giới hạn trên

<img src="https://user-images.githubusercontent.com/43769314/88498546-5ef55280-cffe-11ea-99ec-8d32944ce40c.png" width="720">

*Biểu đồ 1-2*

Điều đó cho ta cảm giác rằng có một điều gì đó không ổn ở đây, thật vậy hãy cùng nhìn vào biểu đồ 1-3 dưới đây (phản ánh chi phí cho mỗi dòng code sau mỗi lần relase)

<img src="https://user-images.githubusercontent.com/43769314/88498599-8ba96a00-cffe-11ea-8dcf-1419ac0fcc87.png" width="720">

*Biểu đồ 1-3*

Biều đồ trên cho thấy Business model hiện tại sẽ làm giảm đi lợi nhuận cũng như tốc độ phát triển của doanh nghiệp, vậy đâu là nguyên nhân khiến cho chi phí của mỗi dòng code sau lần relase thứ 8 lại **tăng 40 lần** so với lần relase thứ 1

#### Những dấu hiệu của sự sụp đổ

Khi:
1. Thiếu chú ý khi thiết kế
2. Code "không sạch"

Thì đều sẽ dẫn đến những hệ quả như trên

<img src="https://user-images.githubusercontent.com/43769314/88499080-d972a200-cfff-11ea-87de-dcdfac696520.png" width="720">

*Biểu đồ 1-4*

Cùng nhìn vào biểu đồ trên "khả năng code" giảm dần sau mỗi lần relase. Từ 100% (relase 1) và chạm đáy ở relase 4. Nhìn từ quan điểm của một developer có thể có ai đó trong team không hoàn thành nhiệm vụ. Nhưng thực tế thì khác, họ vẫn làm nhưng THAY VÌ **phát triển tính năng mới** họ CHỈ **thực hiện những biện pháp ngắn hạn** nhằm ĐỐI ỨNG với những **lỗi hệ thống phát sinh**

#### Quan điểm của những người làm "kinh doanh"

<img src="https://user-images.githubusercontent.com/43769314/88508185-1a2ae500-d019-11ea-8319-1d8d1a26256c.png" width="720">

*Biểu đồ 1-5*

Cùng nhìn vào biểu đồ 1-5 và 1-2 ta đều thấy rằng số tiền phải trả cho dev dù tăng nhưng số lượng các dòng code mới cũng như tính năng mới đều không gia tăng đáng kể. Lúc này những người làm kinh doanh chỉ có thể tức giận với các dev phải không nào?

#### Chúng ta đã làm sai điều gì?

Thông thường các dev đều muốn đưa sản phẩm của mình ra thị trường sớm nhất có thể, họ đều có chung ý khi

> Sau này refactor code cũng được

Thế nhưng áp lực từ thị trường + việc thêm những tính năng mới sẽ khiến cho các dev KHÔNG MUỐN refactor lại code, và đó là nguyên nhân dẫn đến sự sụp đổ sau này của hệ thống. Đồng thời với đó là hiệu suất code giảm đi sau này

Vậy nên bài học ở đây đó là

> Thiết kế cẩn thận, code "sạch sẽ" ngay từ đầu vẫn sẽ "nhanh hơn" so với việc code nhanh, có sản phẩm nhanh nhất có thể

Đồng thời

> Việc tái cấu trúc lại project cũng không đem lại quá nhiều ý nghĩa

Ví dụ

<img src="https://user-images.githubusercontent.com/43769314/88515406-a2fc4d80-d026-11ea-89da-1e0bbf90c1de.png" width="720">

*Biểu đồ 1-6*

Ở biểu đồ trên việc áp dụng TDD giúp cho công việc được tiến hành nhanh hơn là khi không áp dụng TDD

### Chapter 2: Story about twice value

> Các hệ thống phần mềm (Software system) đều chia sẻ 2 giá trị với stack holder: HÀNH ĐỘNG và CẤU TRÚC

Các dev thường chỉ tập trung vào 1 giá trị duy nhất (cũng là giá trị không quan trọng)

#### HÀNH ĐỘNG - Behaviour

Đa phần các dev đều nghĩ công việc của mình là VIẾT CODE để PASS các yêu cầu có trong bản thiết kế và DEBUG nếu có lỗi =====> SUY NGHĨ SAI LẦM

#### Architecture

Bản chất "Soft" của phần mềm "Software" đó chính là ĐƠN GIẢN HOÁ CÁC HÀNH ĐỘNG CỦA MÁY TÍNH
