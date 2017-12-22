---
order: 6
title: 带渐变动画
---

带渐变动画的占位（需要css3支持）

```jsx
import Placeholder from "@sdp.nd/react-placeholder";

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
