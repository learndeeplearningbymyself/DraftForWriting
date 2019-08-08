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

Rõ ràng ảnh phía dưới cho ta cảm giác
