Form Design Pattern

# Chapter 1: Registration form

Chúng ta tạo ra Registration form là để muốn người dùng "kết nối sâu" với ứng dụng của mình, nhưng thực sự thì không người dùng nào muốn điền vào Registration form, họ chỉ quan tâm đến những gì nhận được từ dịch vụ mà chúng ta cung cấp

Một Registration form cơ bản thường sẽ gồm 4 fields, tương ứng với đó là 4 labels

<img width="360" src="https://user-images.githubusercontent.com/43769314/76191512-dc245480-6222-11ea-8206-c4fcb8aae83a.png">

## Labels

Laura Kalbag đã đưa ra 4 yếu tố chính giúp cải thiện UX cho sản phẩm của bạn
- Visual: làm cho nó dễ nhìn
- Auditory: làm cho nó dễ nghe
- Motor: làm cho nó dễ để tương tác
- Cognitive: làm cho nó dễ hiểu

Việc có label cũng giúp cho người dùng dễ nhận biết form element hơn, đồng thời cũng sẽ mở rộng không gian hit với element (chỉ cần click vào label sẽ tự động focus vào element)

Cách map giữa **label** vs **input** khá đơn giản

```html
<label for="input_id">VALUE</label>
<input id="input_id" />
```

Đối với **button**, vì bản thân text trong nó đã đóng vai trò label nên ta **không cần map label cho **button**

> Label không chỉ giúp cho những người dùng gặp vấn đề về tương tác mà còn hữu ích đối với cả người dùng thường khi tương tác với form

## Placeholders

Đóng vai trò hướng dẫn cho người dùng về cách nhập form (đặc biệt với các fields phức tạp như password field), thường có màu ghi để phân biệt với input của người dùng 