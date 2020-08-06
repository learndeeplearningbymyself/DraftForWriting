# Prop Drilling

※ Bài viết được dịch từ nguồn: https://kentcdodds.com/blog/prop-drilling

*Prop Drilling là gì, tại sao nó lại có những ưu điểm cũng như những nhược điểm, và làm thế nào để tránh được các vấn đề thường gặp với nó*

Mục tiêu của bài viết này không chỉ giúp bạn hiểu rõ prop drilling là gì (prop drilling còn được gọi với tên khác là "threading") mà còn giúp bạn có thể tránh được các vấn đề thường gặp với nó.

## Prop Drilling là gì?

Prop drilling (còn được gọi là "threading") là thuật ngữ chỉ tiến trình mà bạn phải đi qua để có thể lấy dữ liệu cho các phần của React component tree. Cùng quan sát một ví dụ đơn giản với "stateful component" (một ví dụ ưa thích của tôi):

```javascript
function Toggle() {
  const [on, setOn] = React.useState(false)
  const toggle = () => setOn(o => !o)
  return (
    <div>
      <div>The button is {on ? 'on' : 'off'}</div>
      <button onClick={toggle}>Toggle</button>
    </div>
  )
}
```

Chúng ta hãy thử chia nó thành 2 components:

```javascript
function Toggle() {
  const [on, setOn] = React.useState(false)
  const toggle = () => setOn(o => !o)
  return <Switch on={on} onToggle={toggle} />
}

function Switch({on, onToggle}) {
  return (
    <div>
      <div>The button is {on ? 'on' : 'off'}</div>
      <button onClick={onToggle}>Toggle</button>
    </div>
  )
}
```

Nói một cách đơn giản `Switch` component cần có tham chiếu tới `toggle` và `on` state, vậy nên chúng ta cần truyền `props` ở đây. Cùng refactor lại một lần nữa để thêm một layer khác vào `component tree` của chúng ta

```javascript
function Toggle() {
  const [on, setOn] = React.useState(false)
  const toggle = () => setOn(o => !o)
  return <Switch on={on} onToggle={toggle} />
}

function Switch({on, onToggle}) {
  return (
    <div>
      <SwitchMessage on={on} />
      <SwitchButton onToggle={onToggle} />
    </div>
  )
}

function SwitchMessage({on}) {
  return <div>The button is {on ? 'on' : 'off'}</div>
}

function SwitchButton({onToggle}) {
  return <button onClick={onToggle}>Toggle</button>
}
```

Đây chính là `prop drilling`. Để lấy được `on` state và `toggle` handler ở đúng chỗ ta cần chuyển (drill - thread) props thông qua `Switch` component. Bản thân `Switch` component không cần những giá trị này cho bản thân nó, nhưng ở đây ta vẫn phải chấp nhận và chuyển tiếp các `props` này xuống dưới các components con của nó. 

## Tại sao Prop Drilling lại tốt ?

Bạn đã từng thử sử dụng các biến global trong ứng dụng của mình? Bạn thấy sao về việc một ứng dụng AngularJS tận dụng việc kế thừa biến `$scope` (hoặc đáng sợ hơn là biến `$rootScope`). Lí do mà cộng đồng nói chung đã "tẩy chay" việc sử dụng các cách thức này đó là chúng thường gây ra sự khó hiểu, mập mờ cho data model của ứng dụng.

Sẽ khá khó cho bất kì ai muốn tìm được nơi mà dữ liệu được khởi tạo, được cập nhật cũng như được sử dụng. **Với những tình huống như vậy, việc trả lời câu hỏi "Liệu tôi có thể thay đổi/ xoá code mà không làm ảnh hưởng đến toàn bộ ứng dụng ?" là vô cùng khó. Và có lẽ câu trả lời duy nhất ở đây đó là phải TỐI ƯU HOÁ code của bạn**

Một lí do khác mà tôi thích ESModules hơn là các biến global đó là nó cho phép chúng ta có thể hiểu rõ hơn về các chỗ mà biến được sử dụng, theo dõi giá trị dễ dàng hơn, giảm thiểu đi ảnh hưởng mà các thay đổi của bạn sẽ tác động đến toàn bộ ứng dụng.

Prop drilling ở mức độ đơn giản nhất đó là việc bạn truyền các giá trị qua các views trong ứng dụng của bạn. Việc này sẽ giúp bạn rất nhiều, giả sử khi bạn đang ở `Toggle` component và muốn refactor `on` state thành enum, sẽ khá dễ dàng để tracking nó chỉ bằng việc đọc code (mà không càn chạy code). Chìa khoá ở đây chính là SỰ TƯỜNG MINH - RÕ RÀNG

## Những vấn đề nào mà prop drilling có thể gây ra ?

Trong ví dụ phía trên, mọi thứ trông có vẻ rất tốt. Nhưng trong thực tế, khi ứng dụng của bạn đi vào hoạt động và ngày một "phình to" (bạn phải chuyền dữ liệu qua nhiều layers), thì việc di chuyển, cập nhật code lại là một vấn đề rất khác cho một vài use cases như sau:

- Refactor shape của dữ liệu (VD: `{user: {name: 'Joe West'}}` => `{user: {firstName: 'Joe', lastName: 'West'}}`)
- Over-forwarding props (truyền quá nhiều props không cần thiết) do việc di chuyển component cần truyền "một vài" props mà component không thực sự cần đến
