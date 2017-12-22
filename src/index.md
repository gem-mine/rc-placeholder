---
category: Components
subtitle: 占位
type: Feedback
title: Placeholder
---

占位组件。

## UEDC 编号

* Image-w：设置 customPlaceholder 自定义占位效果

## 何时使用

用于页面和区块的加载中状态。

## API

```jsx
<Placeholder type="media" rows={7} ready={this.state.ready}>
  <MyComponent />
</Placeholder>
```

### Placeholder API

| API        | 说明         | 类型            |
| ---------- | ------------ | --------------- |
| TextBlock  | 文本占位     | React.Component |
| MediaBlock | 多媒体占位   | React.Component |
| TextRow    | 单行文本占位 | React.Component |
| RectShape  | 矩形占位     | React.Component |
| RoundShape | 圆形占位     | React.Component |

### Placeholder props

| 参数                 | 说明                                                           | 类型          | 默认值             |
| -------------------- | -------------------------------------------------------------- | ------------- | ------------------ |
| children             | 需要使用占位效果的页面或区块                                   | node\|element | 无默认值，必填属性 |
| ready                | 数据是否已经获取，为 false 时显示占位                          | boolean       | 无默认值，必填属性 |
| delay                | 延迟显示占位效果的时间（防止闪烁）                             | number (毫秒) | 0                  |
| firstLaunchOnly      | 是否只出现一次。ready 第一次为 false 时，才出现占位效果        | boolean       | false              |
| showLoadingAnimation | 是否显示占位动画                                               | boolean       | false              |
| type                 | 占位效果类型，可选值为 `text` `media` `textRow` `rect` `round` | string        | 'text'             |
| rows                 | 占位文本行数                                                   | number        | 无默认值，必填属性 |
| color                | 占位效果背景颜色                                               | string        | '#CDCDCD'          |
| customPlaceholder    | 自定义占位元素                                                 | node\|element | -                  |
