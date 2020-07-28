# Clean Architect

※ Mọi hình ảnh trong bài dịch đều được lấy từ sách 「Clean Architecture 達人に学ぶソフトウェアの構造と設計」

## Part 2: Starting with the bricks: Programming Paradigms
### Chapter 3: Paradigm overview

Chương này sẽ giới thiệu về:
- Lập trình cấu trúc
- Lập trình hướng đối tượng
- Lập trình hàm

#### Lập trình cấu trúc

> Áp dụng trực tiếp các quy tắc lên các câu điều khiển di chuyển

VD: thay đổi **goto** thành **if/then/else**

#### Lập trình hướng đối tượng

> Áp dụng gián tiếp các quy tắc lên các câu điều khiển di chuyển

#### Lập trình hàm

Không trực tiếp thay đổi giá trị của biến

> Áp dụng các quy tắc cho các biểu thức giá trị đầu vào

#### Kết luận

Khi đi sâu vào architecture chúng ta sẽ:
- Sử dụng **lập trình hàm** đối với việc bố trí, thiết lập access rules cho data
- Tạo ra các modules với nhiệm vụ riêng bằng **lập trình cấu trúc**
- Sử dụng nguyên tắc đa hình trong **lập trình hướng đối tượng**

Có 3 vấn đề chúng ta cần quan tâm ở đây
- Phân chia components
- Quản lí dữ liệu
- Tính năng

### Chương 4: Lập trình hướng đối tượng