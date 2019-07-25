# Ant Design

Nội dung dịch từ nguồn: https://ant.design/docs/spec/proximity

## Proximity

Khoảng cách có vai trò quan trọng trong tổ chức layout, phân biệt các phần tử với nhau, qua đó tạo nên hệ thống phân cấp thông tin

### Mối liên hệ giữa khoảng cách dọc (vertical spacing)

Ant Design sử dụng 3 kiểu khoảng cách dọc
- small spacing: 8px
- middle spacing: 16px
- large spacing: 24px

<img src="https://user-images.githubusercontent.com/43769314/61839651-5ccb5600-aec9-11e9-8a65-fe6001ee4181.png">

Nguồn: https://ant.design/docs/spec/proximity

> Note: Trong Ant Design, y = 8 + 8 * n (n >= 0), y là vertical spacing, 8 là [basic spacing]

Qua đó ta thấy, để tăng mức độ phân cấp cho thông tin ta có thể **thêm** hoặc **bớt** đi các **basic spacing**.

### Mối liên hệ giữa khoảng cách ngang (horizontal spacing)

Để đảm bảo sự tương thích với các kích cỡ màn hình khác nhau, trong **horizontal direction** ta sử dụng grid layout để sắp xếp các phần tử

Horizontal spacing gồm 2 kiểu
- Outer: Khoảng cách giữa các components với nhau
- Inner: Khoảng cách giữa các thành phần trong 1 component

<img src="https://user-images.githubusercontent.com/43769314/61840300-a3ba4b00-aecb-11e9-9928-7351be0f75b2.png">

Nguồn: https://ant.design/docs/spec/proximity

## Alignment

Con người có xu hướng tiếp nhận, hiểu, đánh giá vấn đề dựa vào cái nhìn đầu tiên.
Trong thiết kế, việc căn gióng có vai trò quan trọng trong truyền tải thông tin tới người dùng

### Text Alignment

Nếu độ dài của các từ cũng như đoạn văn là quá ngắn thì cần có **visual starting point**

- Căn lề cho title và text sang trái, sử dụng 1 **visual starting point**
- Không nên để cho title và text bắt đầu ở những visual points khác nhau (ngoại trừ khi sự khác biệt giữa title và text được nhấn mạnh)

### Form Alignment

Căn lề cho các dấu **:** trong form sẽ giúp tăng tốc độ cho người dùng hoàn thiện form.

<img src="https://user-images.githubusercontent.com/43769314/61841543-19281a80-aed0-11e9-9127-58e61af257ae.png">

Nguồn: https://ant.design/docs/spec/proximity

### Number Alignment

Để so sánh nhanh các số, ta nên căn lề phải, cũng như sử dụng cùng một số lượng chữ số sau dấu phảy.

<img src="https://user-images.githubusercontent.com/43769314/61841636-5e4c4c80-aed0-11e9-9893-3af7a8bc1e7f.png">

Nguồn: https://ant.design/docs/spec/proximity

## Contrast

Tương phản giúp tăng mức độ thú vị cho page cũng như tạo ra hệ thống phân cấp thông tin giúp người dùng tra cứu thông tin nhanh hơn

### Mối liên hệ chính phụ của tương phản

Để giúp người dùng đưa ra quyết định nhanh hơn, các **hành động quan trọng** hoặc **hành động có tần suất cao** nên được **nhấn mạnh** (trong form, modal)

> Note: Ngoài cách nhấn mạnh item chính, ta còn có thể làm yếu đi các items phụ

<img src="https://user-images.githubusercontent.com/43769314/61841899-45906680-aed1-11e9-8f9e-1b4a6689a45b.png">

Nguồn: https://ant.design/docs/spec/proximity
