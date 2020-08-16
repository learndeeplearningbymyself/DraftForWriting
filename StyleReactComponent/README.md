## So sánh 8 cách style cho React component

※ Bài viết được dịch từ nguồn: https://www.sitepoint.com/react-components-styling-options/

**Tôi đã và đang làm việc cùng một vài developers trong các dự án sử dụng ReactJS (họ đều là những developers có ít nhiều kinh nghiệm với ReactJS). Chúng tôi đã và đang giải quyết các vấn đề điên rồ như: [xử lí cách khởi tạo state "quái dị" của Redux](https://blog.praveen.science/handling-the-weird-way-of-redux-state-initialisation/) và [giúp cho axios request payload hoạt động được với PHP và hiểu được cơ chế phía background](https://blog.praveen.science/making-axios-request-payload-work-with-php/). Bài viết này làm nảy sinh ra một câu hỏi về cách style cho các React components.**

## Các cách tiếp cận đa dạng cho styling

Có khá nhiều cách để style các React components. Chọn đúng phương thức không hẳn đã là hoàn hảo tuyệt đối. Thay vào đó quyết định của bạn phải hữu ích cho use case của bạn và trên hết đó là định hình đích đến cho công việc của bạn. Ví dụ, tôi quyết định [sử dụng Noty cho notifications trong ứng dụng ReactJS của mình](https://blog.praveen.science/notifications-in-react-js-using-noty/) và đương nhiên cũng phải styling cho plugins.

Một vài mục tiêu của tôi khi trả lời câu hỏi gồm những điều như sau:

- Global namespacing
- Dependencies
- Reusability
- Scalability
- Dead-code Elimination

Hiên nay có khoảng 8 cách styling cho React components được sử dụng rộng rãi trên toàn thế giới:

- Inline CSS
- Normal CSS
- CSS in JS
- Styled Components
- CSS modules
- Sass & SCSS
- Less
- Stylable

Với mỗi cách, tôi sẽ đề cập đến: sự cần thiết của các dependencies, mức độ khó và liệu đó có phải là cách tiếp cận tốt hay không.

### Inline CSS

- Dependencies: **Không cần**
- Mức độ: **Dễ**
- Đánh giá cách tiếp cận: **Tệ nhất**

Tôi không nghĩ mình cần giới thiệu quá nhiều về phương thức này. Nó chỉ đơn thuần là việc chúng ta chèn CSS styling trực tiếp vào các thẻ HTML hoặc JSX. Bạn có thể include một Javascript object cho CSS trong các React components. Cũng sẽ có một vài hạn chế đó là việc thay thế các dấu `-` bằng `camelCase text`. Bạn có thể style chúng theo hai cách thông qua việc sử dụng Javascript object như ví dụ dưới đây:

**Ví dụ**

```javascript
import React from "react";

const spanStyles = {
  color: "#fff",
  borderColor: "#00f"
};

const Button = props => (
  <button style={{
        color: "#fff",
  borderColor: "#00f"
    }}>
    <span style={spanStyles}>Button Name</span>
  </button>
);
```

### Regular CSS

- Dependencies: **Không cần**
- Mức độ: **Dễ**
- Đánh giá cách tiếp cận: **Tạm ổn**

Regular CSS là một cách tiếp cận khá phổ biến, tối ưu hơn so với inline CSS. Các styles có thể được import và dùng cho nhiều pages, elements khác nhau không giống như inline CSS - chỉ được dùng cho một element cụ thể nào đó. Normal CSS có khá nhiều ưu điểm, ví dụ như: giảm được kích cỡ của file với một cấu trúc code "clean".

Bạn có thể dễ dàng maintain, cũng như thay đổi, custom bất kì styles nào mà bạn muốn. Tuy nhiên đây cũng là vấn đề đối với các project lớn hơn khi không có sự nhất trí về cách code của team

```css
a:link {
  color: gray;
}
a:visited {
  color: green;
}
a:hover {
  color: rebeccapurple;
}
a:active {
  color: teal;
}
```

### CSS in JS

- Dependencies: `jss`, `jss-preset-default`, `jss-cli`
- Mức độ: **Dễ**
- Đánh giá cách tiếp cận: **Khá tốt**

CSS in JS là một phương pháp cho phép bạn sử dụng JS để styling cho component. Những đặc điểm cơ bản của phương pháp này:
- Dựa trên định nghĩa (object - style object)
- Conflict-free
- Có khả năng tái sử dụng

CSS in JS có thể được compile: tại browser, phía server, build time trong Node. Đứng từ góc độ các components, bạn không cần phải maintain cả tá code style sheets.

CSS in JS được compile bởi `JS-to-CSS compiler`

VD:

```javascript
import React from "react";
import injectSheet from "react-jss";

// Create your Styles. Remember, since React-JSS uses the default preset,
// most plugins are available without further configuration needed.
const styles = {
  myButton: {
    color: "green",
    margin: {
      // jss-expand gives more readable syntax
      top: 5, // jss-default-unit makes this 5px
      right: 0,
      bottom: 0,
      left: "1rem"
    },
    "& span": {
      // jss-nested applies this to a child span
      fontWeight: "bold" // jss-camel-case turns this into 'font-weight'
    }
  },
  myLabel: {
    fontStyle: "italic"
  }
};

const Button = ({ classes, children }) => (
  <button className={classes.myButton}>
    <span className={classes.myLabel}>{children}</span>
  </button>
);

// Finally, inject the stylesheet into the component.
const StyledButton = injectSheet(styles)(Button);
```

### Styled Components

- Dependencies: `styled-components`
- Mức độ: **Trung bình**
- Đánh giá cách tiếp cận: **Khá tốt**

Đây là một ví dụ của phương pháp **CSS in JS** được đề cập ở trên. Về cơ bản nó đem lại cho bạn những tiện ích không có trong CSS như **nesting**.

Ngoài ra nó còn cho phép bạn style cho component thông qua các biến định nghĩa bằng JS

Bạn có thể tạo một React component với style đi kèm với nó, thay vì phải tạo một file CSS riêng. Có sử dụng props tương tự như class

VD:

```javascript
import React from "react";
import styled, { css } from "styled-components";

const Button = styled.button`
  cursor: pointer;
  background: transparent;
  font-size: 16px;
  border-radius: 3px;
  color: palevioletred;
  margin: 0 1em;
  padding: 0.25em 1em;
  transition: 0.5s all ease-out;
  ${props =>
    props.primary &&
    css`
      background-color: white;
      color: green;
      border-color: green;
    `};
`;

export default Button;
```

### CSS modules

- Dependencies: **css-loader**
- Mức độ: **Khó**
- Đánh giá cách tiếp cận: **Khá tốt**

Chắc hẳn bạn đã từng gặp vấn đề với CSS global scope vì nó khiến bạn phải tìm cụ thể về cách hoạt động của từng đoạn CSS một, chưa kể tới việc tổ chức code CSS cũng khá khó khăn.

`CSS Modules` đảm bảo việc mọi styles cho component đều được tập trung ở một chỗ và được áp dụng cho một component cụ thể.

Tính năng `composition` như một công cụ để chia sẻ style (tương tự như `mixin` trong Sass).

VD:

```javascript
import React from "react";
import style from "./panel.css";

const Panel = () => (
  <div className={style.panelDefault}>
    <div className={style.panelBody}>A Basic Panel</div>
  </div>
);

export default Panel;
```

```CSS
.panelDefault {
  border-color: #ddd;
}

.panelBody {
  padding: 15px;
}
```

### Sass & SCSS

- Dependencies: `node-sass`
- Mức độ: **Dễ**
- Đánh giá cách tiếp cận: **Tốt nhất**

Sass cho rằng đây là ngôn ngữ mở rộng tốt nhất, tối ưu nhất của CSS. Nó được đưa vào các cú pháp mà CSS cơ bản không có như: biến, nested rules, mixin.

VD:

```scss
$font-stack: 'Open Sans', sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

### Less

- Dependencies: `less`, `less-loader`
- Mức độ: **Dễ**
- Đánh giá cách tiếp cận: **Tốt**

Là một `dynamic preprocessor style sheet language` có thể biên dịch thành CSS

Tương tự như Sass nhưng khác biệt ở chỗ: `@` thay vì `$` như Sass

VD: 
```less
@pale-green-color: #4D926F;

#header {
  color: @pale-green-color;
}

h2 {
  color: @pale-green-color;
}
```
