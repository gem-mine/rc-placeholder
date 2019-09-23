---
order: 5
title: 自定义占位
---

自定义占位元素

```jsx
import Placeholder from "@gem-mine/react-placeholder";

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
