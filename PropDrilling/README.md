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
- Under-forwarding props và lạm dụng `defaultProps` nên bạn có thể không nhận ra việc thiếu props (cũng một phần do việc di chuyển component gây ra)
- Đổi tên props kiểu "nửa vời" (VD: `<Toggle on={on} />` render `<Switch toggleIsOn={on} />`) khiến việc theo dõi props sẽ "hack não" hơn.

Và còn khá nhiều tình huống khác khiến cho việc sử dụng prop drilling gây ra những vấn đề khiến bạn đau đầu, đặc biệt là trong quá trình refactoring code.

## Làm cách nào chúng ta có thể tránh được các vấn đề với prop drilling ?

Một trong những điều khiến prop drilling gây ra những vấn đề như trên chính là việc "chia nhỏ" `render` method thành nhiều components một cách không cần thiết. Bạn sẽ thấy bất ngờ về sự đơn giản của một hàm `render` "lớn" so với việc bạn cố gắng "inline" các dòng code của mình nhiều nhất có thể.

Vậy nên, không có bất kì lí do nào khiến cho bạn phải "xé lẻ" `render` method của mình thành các components nhỏ hơn quá sớm cả, hãy chờ cho tới khi bạn nhận thấy có thể tái sử dụng lại nhiều lần các đoạn code thuộc `render` method. Khi đó bạn không nhất thiết phải truyền props quá nhiều lần.

> Có một sự thật thú vị rằng, không hề có kĩ thuật nào "ép" bạn không được viết toàn bộ ứng dụng của mình chỉ trong một React component duy nhất cả. Nó có thể quản lí state của toàn bộ ứng dụng của bạn kèm theo một render method "khổng lồ"... Mặc dù tôi không cổ xuý cho cách làm này nhưng... Hãy thử nghĩ về nó mà xem...

*Note: Tôi cũng có viết một bài blog về chủ đề ["Khi nào nên chia một component thành các components con"](https://kentcdodds.com/blog/when-to-break-up-a-component-into-multiple-components) để bạn có thể tham khảo thêm.*

Một cách khác bạn có thể làm giảm đi các tác động tiêu cực của prop drilling đó là tránh việc sử dụng `defaultProps` cho bất kì component nào cần props. Sử dụng `defaultProps` sẽ làm các lỗi nghiêm trọng khó phát hiện hơn cũng như âm thầm huỷ hoại hệ thống của bạn.

Nếu một phần ứng dụng của bạn cần đến states, hãy giữ chúng ở component cha gần nhất thay vì đặt states ở các level cao hơn (layer cao hơn) trong ứng dụng. Bạn có thể xem thêm về "state management" từ bài blog của tôi: [Application State Management](https://kentcdodds.com/blog/application-state-management-with-react)

Sử dụng [React's Context API](https://kentcdodds.com/blog/how-to-use-react-context-effectively) cho các thành phần thực sự nằm ở các layer thấp trong react component tree. Chúng không hẳn đã cần thiết ở *mọi nơi* trong ứng dụng (bạn có thể render ra một provider ở bất kì đâu trong ứng dụng). Điều này có thể giúp bạn tránh ít nhiều các vấn đề thường gặp với prop drilling. Cũng có một điều đáng lưu ý là context có thể đưa chúng ta trở lại với thời kì của global variables (các biến toàn cục). Sự khác biệt ở đây đó chính là cách mà API được thiết kế, nó khiến cho việc tìm source của context trở nên tương đối dễ dàng

## Tổng kết

Prop drilling có những ưu, nhược điểm nhất định. Tham khảo những ví dụ đã đề cập ở trên có thể giúp cho ứng dụng của bạn trở nên dễ maintain hơn. Chúc may mắn
