---
order: 10
title: 直接使用内置占位类型
---

直接使用内置占位类型，通常用来做自定义占位

```jsx
import Placeholder from "@gem-mine/react-placeholder";
import { TextBlock, MediaBlock, TextRow, RectShape, RoundShape } from "@gem-mine/react-placeholder/../placeholders";

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
