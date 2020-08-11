## React Context

※ Dịch từ nguồn: https://reactjs.org/docs/context.html

> Context cung cấp cách thức để truyền dữ liệu đi khắp component tree mà không cần phải truyền props xuống các tầng thấp hơn một cách thủ công

Trong một ứng dụng React điển hình, dữ liệu được truyền theo hướng top-down (componet cha xuống component con) thông qua props, nhưng với các kiểu dữ liệu điển hình như (locale hay UI theme), thường được hầu hết các component sử dụng thì việc phải truyền các dữ liệu dạng này dưới hình thức props trở nên khá bất tiện. Context cung cấp một cách thức để truyền các loại dữ liệu kiểu này giữa các components mà không phải truyền chúng thông qua props một cách tường minh.

### Khi nào sử dụng context

Context được thiết kế để share các dữ liệu theo kiểu "global" như `authenticated user`, `theme` hoặc `ngôn ngữ`. Ví dụ như đoạn code dưới đây, chúng ta sẽ style cho Button component thông qua việc truyền `theme prop`

```javascript
class App extends React.Component {
  render() {
    return <Toolbar theme="dark" />;
  }
}

function Toolbar(props) {
  // The Toolbar component must take an extra "theme" prop
  // and pass it to the ThemedButton. This can become painful
  // if every single button in the app needs to know the theme
  // because it would have to be passed through all components.
  return (
    <div>
      <ThemedButton theme={props.theme} />
    </div>
  );
}

class ThemedButton extends React.Component {
  render() {
    return <Button theme={this.props.theme} />;
  }
}
```

Bằng việc sử dụng context chúng ta có thể tránh được việc truyền props thông qua các components trung gian

```javascript
// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

// A component in the middle doesn't have to
// pass the theme down explicitly anymore.
function Toolbar() {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

class ThemedButton extends React.Component {
  // Assign a contextType to read the current theme context.
  // React will find the closest theme Provider above and use its value.
  // In this example, the current theme is "dark".
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```

### Trước khi bạn sử dụng context

Chỉ nên sử dụng context với những dữ liệu được sử dụng bởi *rất nhiều components*. Vì việc lạm dụng context sẽ khiến việc tái sử dụng component trở nên khó khăn hơn

**Nếu bạn chỉ muốn tránh việc truyền quá nhiều props qua các components trung gian thì việc sử dụng [component composition](https://reactjs.org/docs/composition-vs-inheritance.html) là một giải pháp tốt hơn là context**

Lấy ví dụ như sau: `Page` component truyền `user` và `avatarSize` prop xuống nhiều layer cấp thấp hơn đến các components con là `Link` và `Avatar`

```javascript
<Page user={user} avatarSize={avatarSize} />
// ... which renders ...
<PageLayout user={user} avatarSize={avatarSize} />
// ... which renders ...
<NavigationBar user={user} avatarSize={avatarSize} />
// ... which renders ...
<Link href={user.permalink}>
  <Avatar user={user} size={avatarSize} />
</Link>
```

Cảm giác rằng việc truyền props qua các components trung gian để rồi chỉ duy nhất một component là `Avatar` sử dụng chúng thật sự là thừa thãi

Một cách khác để giải quyết vấn đề này mà **không cần context** đó là [truyền thẳng Avatar component xuống](https://reactjs.org/docs/composition-vs-inheritance.html#containment) vì thế các components trung gian sẽ không cần phải biết đến `user` và `avatarSize` props:

```javascript
function Page(props) {
  const user = props.user;
  const userLink = (
    <Link href={user.permalink}>
      <Avatar user={user} size={props.avatarSize} />
    </Link>
  );
  return <PageLayout userLink={userLink} />;
}

// Now, we have:
<Page user={user} avatarSize={avatarSize} />
// ... which renders ...
<PageLayout userLink={...} />
// ... which renders ...
<NavigationBar userLink={...} />
// ... which renders ...
{props.userLink}
```

Với sự thay đổi này chỉ duy nhất top-most `Page` component là biết đến việc `Avatar` component sử dụng `user` và `avatarSize` props.

Việc *đảo ngược kiểm soát* này sẽ khiến code của bạn "sạch hơn" và giảm đi số lượng props phải truyền, cũng như tăng cường sự kiểm soát ở các root components (components cha). Tuy nhiên đây không hẳn đã là sự lựa chọn tốt nhất cho mọi trường hợp: việc di chuyển các xử lí lên các components cha sẽ khiến cho các components này trở nên "phức tạp" hơn so với các components cấp thấp hơn (các components này sẽ trở nên "khả chuyển" hơn).

Bạn không bị giới hạn bởi việc chỉ có duy nhất một child cho một component. Bạn có thể truyền nhiều childs hoặc kể cả có nhiều "slots" riêng biệt cho các childs, [như tài liệu ở đây đã đề cập](https://reactjs.org/docs/composition-vs-inheritance.html#containment)

```javascript
function Page(props) {
  const user = props.user;
  const content = <Feed user={user} />;
  const topBar = (
    <NavigationBar>
      <Link href={user.permalink}>
        <Avatar user={user} size={props.avatarSize} />
      </Link>
    </NavigationBar>
  );
  return (
    <PageLayout
      topBar={topBar}
      content={content}
    />
  );
}
```

Đôi khi có những dữ liệu được khá nhiều components ở các layers khác nhau trong component tree truy cập. Context cho phép bạn "broadcast" các dữ liệu như vậy cũng như thay đổi và cập nhật chúng. Các ví dụ trên đây đều đơn giản hơn rất nhiều so với các trường hợp trong thực tế (quản lí locale, theme hay cache data)
