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

### Chương 4: Lập trình hướng đối tượng (Object Oriented Programming - OOP)

Bản chất của thuật ngữ hướng đối tượng (object oriented) nghĩa là bao hàm "function" và "data"

#### Encapsulation

Khái niệm OO trong OOP nghĩa là đóng gói "data" và "function", tạo ra một lằn ranh đối với bên ngoài.
1. Từ bên ngoài không thể thấy được data
2. Từ bên ngoài chỉ thấy được một phần function

===> Private member data, Public member function

Trong ngôn ngữ "phi OO" là ngôn ngữ C, encapsulation được triển khai theo một cách khá "hoàn hảo"

```C
// point.h - header file

struct Point;
struct Point* makePoint(double x, double y);
double distance(struct Point *p1, struct Point *p2);

// point.c

#include "point.h"
#include <stdlib.h>
#include <math.h>

struct Point {
  double x,y;
};

struct Point* makepoint(double x, double y) {
  struct Point* p = malloc(sizeof(struct Point));
  p->x = x;
  p->y = y;
  return p;
}

double distance(struct Point* p1, struct Point* p2) {
  double dx = p1->x - p2->x;
  double dy = p1->y - p2->y;
  return sqrt(dx*dx + dy*dy);
}
```

Những người sử dụng file **point.h** có thể gọi hàm **distance** hoặc **makepoint** nhưng họ tuyệt nhiên không hề biết gì về cấu trúc bên trong của **struct Point**. Ta định nghĩa data structure và function signature trong header file nhưng triển khai chúng trong implement file (.c file)

Nhưng với ngôn ngữ OO là C++ thì điều này bị phá vỡ, do yêu cầu của compiler mà các "member data" phải được đưa vào **header file**

```C++
// point.h

class Point {
  public:
    Point(double x, double y);
    double distance(const Point& p) const;
  private:
    double x;
    double y;
}

// point.cc
#include "point.h"
#include <math.h>

Point::Point(double x, double y)
: x(x), y(y)
{}

double Point::distance(const Point& p) const {
  double dx = x-p.x;
  double dy = y-p.y;
  return sqrt(dx*dx + dy*dy);
}
```

Người dùng của header file sẽ biết về member data là x, y. Compiler sẽ ngăn người dùng truy cập chúng tuy nhiên người dùng vẫn sẽ biết về sự tồn tại của chúng, ngoài ra khi các member data này thay đổi thì file **point.cc** sẽ phải compile lại.

Vậy là tính **Encapsulation** đã BỊ PHÁ BỎ

Thay vào đó các ngôn ngữ OO hiện đại thêm vào đó các từ khoá **public**, **protected**, **private** để điều khiển truy cập của người dùng

> Kết luận: khó có thể nói các ngôn ngữ OO phụ thuộc mạnh mẽ vào Encapsulation đến vậy

#### Extends

```C++
TODO: insert CODE HERE
```

Ở ví dụ trên NamedPoint có thể coi như một tập rộng hơn của Point và có thể sử dụng tương tự như Point (thực ra NamedPoint ở đây là một cách giả mạo Point)

Thực ra chúng ta đã có thể mô phỏng Extends trước khi OO language xuất hiện. Thực sự thì OO language không hẳn đã mang đến cho chúng ta một thứ gì đó mới mẻ mà thực chất nó chỉ giúp cho những dữ liệu "giả" trở nên tiện lợi hơn mà thôi

#### Polymorphism