---
order: 8
title: 延迟出现占位
---

通过设置 delay，控制延迟显示占位效果的时间（防止闪烁），单位是毫秒。

```jsx
import Placeholder from "@sdp.nd/react-placeholder";

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
