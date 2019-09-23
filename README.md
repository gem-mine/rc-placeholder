# 占位

---

占位组件，根据[react-placeholder](https://github.com/buildo/react-placeholder)做兼容ie8调整

## 浏览器支持

| ![IE](https://raw.github.com/alrra/browser-logos/master/internet-explorer/internet-explorer_48x48.png) | ![Chrome](https://raw.github.com/alrra/browser-logos/master/chrome/chrome_48x48.png) | ![Firefox](https://raw.github.com/alrra/browser-logos/master/firefox/firefox_48x48.png) | ![Opera](https://raw.github.com/alrra/browser-logos/master/opera/opera_48x48.png) | ![Safari](https://raw.github.com/alrra/browser-logos/master/safari/safari_48x48.png) |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| IE 8+ ✔                                                                                                | Chrome 31.0+ ✔                                                                       | Firefox 31.0+ ✔                                                                         | Opera 30.0+ ✔                                                                     | Safari 7.0+ ✔                                                                        |

## 本地运行

```
npm install
npm run start
```

### 文本占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder type="text" ready={false} rows={6} color="#E0E0E0">
    <div />
  </Placeholder>,
  mountNode
);
```

### 多媒体占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder type="media" ready={false} rows={6}>
    <div />
  </Placeholder>,
  mountNode
);
```

### 单行文本占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder type="textRow" ready={false} color="#E0E0E0">
    <div />
  </Placeholder>,
  mountNode
);
```

### 矩形占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder type="rect" ready={false} color='#E0E0E0' style={{ width: 50, height: 50 }}>
    <div />
  </Placeholder>,
  mountNode
);
```

### 圆形占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder type="round" ready={false} color='#E0E0E0' style={{ width: 50, height: 50 }}>
    <div />
  </Placeholder>,
  mountNode
);
```

### 自定义占位元素

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder
    customPlaceholder={
      <div style={{ color: "blue", backgroundColor: "yellow" }}>
        I'm a custom placeholder!
      </div>
    }
    ready={false}
  >
    <div />
  </Placeholder>,
  mountNode
);
```

### 带渐变动画的占位（需要css3支持）

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

ReactDOM.render(
  <Placeholder
    showLoadingAnimation={true}
    type="media"
    ready={false}
    rows={4}
  >
    <div />
  </Placeholder>,
  mountNode
);
```

### 只出现一次

设置 firstLaunchOnly 属性为 true，ready 第一次为 false 时，占位符出现。

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = { ready: false };
  }
  toggleReady = () => {
    this.setState({ ready: !this.state.ready });
  };
  render() {
    return (
      <div>
        <button onClick={this.toggleReady}>
          toggle "ready" state (ready is "{String(this.state.ready)}")
        </button>
        <Placeholder
          firstLaunchOnly={true}
          ready={this.state.ready}
          rows={4}
          color="#E0E0E0"
        >
          <div
            style={{
              padding: "10px",
              backgroundColor: "rgb(240, 240, 240)",
              color: "red"
            }}
          >
            I'm the real component!
          </div>
        </Placeholder>
      </div>
    );
  }
}

ReactDOM.render(<App />, mountNode);
```

### 延迟出现占位

通过设置 delay，控制延迟显示占位效果的时间（防止闪烁），单位是毫秒。

```jsx
import Placeholder from "@gem-mine/rc-placeholder";

class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = { ready: true };
  }
  toggleReady = () => {
    this.setState({ ready: !this.state.ready });
  };
  render() {
    return (
      <div>
        <button onClick={this.toggleReady}>
          toggle "ready" state (ready is "{String(this.state.ready)}")
        </button>
        <Placeholder
          delay={1000}
          ready={this.state.ready}
          rows={4}
          color="#E0E0E0"
        >
          <div
            style={{
              padding: "10px",
              backgroundColor: "rgb(240, 240, 240)",
              color: "red"
            }}
          >
            I'm the real component!
          </div>
        </Placeholder>
      </div>
    );
  }
}

ReactDOM.render(<App />, mountNode);
```

### 直接使用内置占位类型

直接使用内置占位类型，通常用来做自定义占位

```jsx
import Placeholder from "@gem-mine/rc-placeholder";
import { TextBlock, MediaBlock, TextRow, RectShape, RoundShape } from "@gem-mine/rc-placeholder/placeholders";

const awesomePlaceholder = (
  <div className="my-awesome-placeholder">
    <RectShape color="blue" style={{ width: 300, height: 80 }} />
    <TextBlock rows={7} color="yellow" />
  </div>
);
ReactDOM.render(
  <Placeholder ready={false} customPlaceholder={awesomePlaceholder}>
    <div />
  </Placeholder>,
  mountNode
);
```


## 文档 & 示例

http://localhost:8004
