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

Dù **input** có thuộc tính **placeholder** nhưng không nhất thiết là ta phải sử dụng chúng, ví dụ như sau:

<img width="290" src="https://user-images.githubusercontent.com/43769314/76376146-efeaca80-638a-11ea-9f95-295fa6224e47.png">

Bản thân label **First name** cũng đủ nói lên ý nghĩa của text input nên việc thêm placeholder **Enter your first name** là hoàn toàn không cần thiết

Placeholder có khá nhiều ưu điểm như:
- Nhỏ gọn
- Không tốn không gian vì **nó nằm trong input**

Nhưng đây cũng là vấn đề khi chúng ta muốn đem lại cho người dùng một sự gợi ý nào đó về dữ liệu cần nhập. Có thể kể ra như sau:
- Placeholder thường biến mất khi người dùng nhập liệu
- Đôi khi nội dung khó nhớ, có thể khiến người dùng nhập dữ liệu nhầm
- Màu của placeholder là màu ghi nên sẽ bị mất đi tính tương phản đối với màu nền của input
- Một số browsers không hỗ trợ placeholder
- Placeholder quá dài dẫn đến không hiển thị được hết cho người dùng

<img width="470" src="https://user-images.githubusercontent.com/43769314/76387542-8da1c200-63aa-11ea-8b1b-6c2cfb6f8ed9.png">

Do những vấn đề như trên, thay vì sử dụng placeholder, ta có thể sử dụng hint dưới dạng label như sau:

<img width="475" src="https://user-images.githubusercontent.com/43769314/76387895-33553100-63ab-11ea-8911-38a96c350ca1.png">

## Float Labels

Là một pattern cho việc sử dụng label với vai trò của placeholder. Ban đầu, label sẽ nằm trong input, khi người dùng nhập liệu nó sẽ "trôi" lên trên

<img width="645" src="https://user-images.githubusercontent.com/43769314/76584042-2c026480-651e-11ea-9201-6ba8024fb7c6.png">

Cách làm này khá hay ở những điểm sau
- Tiết kiệm không gian
- Mang tính tối giản cao

Tuy nhiên cũng có khá nhiều nhược điểm
- Vì label và hint là một nên không có không gian cho hint
- Có thể bị cropped
- Độ tương phản thấp (để user phân biệt với giá trị thường), dẫn đến khó đọc

Những yếu tố lạ, cũng như tối giản không hẳn đã giúp cho người dùng thoải mái với UI của bạn - mà thay vào đó UI rõ ràng vẫn là yếu tố quan trọng hơn cả

## The Question Protocol

Một trong những cách tự nhiên nhất để giảm kích cỡ của form đó là sử dụng "question protocol", đây là cách giúp đảm bảo rằng bạn hiểu rõ những gì mà form của mình cần có

VD: liệu form đăng kí có cần phải hỏi người dùng về "first name", "email", hoặc "password" hay không, qua đó giúp đơn giản hoá trải nghiệm của người dùng đối với form

Nếu không quá cần "first name" và "last name" hãy loại bỏ chúng, điều này sẽ giúp giảm một nửa kích cỡ của form

## NO PASSWORD SIGN-IN

Đây là cách đăng nhập không dùng password, chỉ yêu cầu người dùng nhập email, hệ thống sẽ gửi link đến email, click vào link đó, người dùng sẽ ở trạng thái đăng nhập ngay tức thì

Về cơ bản cách này giúp giảm bớt đi 1 field password cho form đăng kí, nhưng nó cũng có ít nhiều nhược điểm như sau:
- Người dùng chưa quá quen với flow này
- Người dùng sẽ nghi vấn về tính bảo mật của ứng dụng
- Người dùng sẽ phải chuyển qua lại giữa ứng dụng mail và ứng dụng của bạn

## PASSPHRASES

Người dùng thường nhập vào các password dễ nhớ và ngắn nhất có thể, nhưng điều đó lại tiềm ẩn nhiều rủi ro về bảo mật. Vậy nên các trang web hiện nay thường yêu cầu người dùng nhập các password

> Min lenght = 8, có chứa kí tự hoa, chữ số, kí tự đặc biệt v..v..

Nhưng đối với người dùng thì điều đó thật phiền phức và khó nhớ, chưa kể vẫn có khả năng tiềm ẩn các nguy cơ về bảo mật khác.

Sử dụng **passphrase** là một giải pháp khá ổn cho 2 vấn đề trên, passphrase là một dạng câu hỏi liên quan đến thông tin cá nhân người dùng nhằm mục đích xác thực người dùng. Ví dụ như:
- Mô tả thú cưng của bạn ?
- ...

Rất đơn giản với người dùng nhưng cũng đảm bảo độ an toàn bảo mật nhất định ("thường thì" các câu trả lời phải có ít nhất 16 kí tự)

Tuy nhiên cách làm này không quá phổ biến và có thể khiến người dùng nghi ngờ về tính bảo mật của nó do người dùng đã quá quen với password-authen.

Vậy nên hãy thay đổi phương thức authen chỉ khi bạn đã nghiên cứu kĩ về người dùng và chuẩn bị kĩ lưỡng nếu bạn không muốn gặp phải một vấn đề khác.

## Field Styling

> Style cho form tuỳ vào tính chất sản phẩm của bạn

## LABEL POSITION

Đa phần chúng ta thường đặt label **bên cạnh** hoặc **phía trên** control/ input

Nhưng việc đặt **phía trên** sẽ có nhiều điểm tích cực hơn. Ví dụ như:
- Tránh bị vỡ layout nếu view-port có kích cỡ nhỏ
- Tránh bị vỡ layout nếu label chiếm nhiều dòng
- Tránh tình trạng label biến mất khi người dùng zoom in màn hình

## LOOK, SIZE, AND SPACE

Mọi thành phần của form nên được biểu thị sao cho đúng ý nghĩa của nó
- TextField nên giống như TextField

Theo như nhận định trên thì việc có placeholder không hẳn là một ý hay vì nó sẽ phá vỡ đi ý nghĩa "hãy điền vào chỗ trống" của TextField

TextField nên được bo viền 4 phía, nếu chỉ bo viền dưới bottom, người dùng có thể nhầm rằng đó là "Separate Line"

Ngoài ra những gì thuộc cùng một nhóm nên được bố trí gần nhau nhất có thể (label và text field)

Cuối cùng, khu vực tap cho label và text field cần đủ lớn, vậy nên chọn cỡ font tối thiểu là 16px, không gian tương tác nhỏ nhất nên chiếm 44pixels

## FOCUS STYLES

Là các bo viền xuất hiện khi chọn text box - để chứng tỏ rằng người dùng đang focus vào element, tuy nhiên đôi khi chúng khá mờ để nhận ra cũng như có màu sắc không được bát mắt

Không nên bỏ đi style này vì nó sẽ làm ảnh hưởng đến trải nghiệm của người dùng, thay vào đó hãy làm đậm hơn bo viền của text box khi nó được focus

```css
input:focus {
  outline: 4px solid #ffbf47;
}
```

## The Email Field

