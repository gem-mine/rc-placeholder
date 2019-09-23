---
order: 7
title: 只出现一次
---

设置 firstLaunchOnly 属性为 true，ready 第一次为 false 时，占位符出现。

```jsx
import Placeholder from "@gem-mine/react-placeholder";

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
