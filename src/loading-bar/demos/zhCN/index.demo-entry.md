# 加载条 Loading Bar

焦虑的安慰剂，疗效尚可。

<n-space vertical>
<n-alert title="使用前提" type="warning">
  如果你想使用加载条，你需要把调用其方法的组件放在 <n-text code>n-loading-bar-provider</n-text> 内部并且注入 <n-text code>loadingBar</n-text>。
</n-alert>
例如：

```html
<!-- App.vue -->
<n-loading-bar-provider>
  <content />
</n-loading-bar-provider>
```

```js
import { useLoadingBar } from 'naive-ui'

// content
export default {
  setup () {
    const loadingBar = useLoadingBar()
    return {
      loading () {
        loadingBar.start()
      }
    }
  }
}
```

</n-space>

## 演示

```demo
basic
```

## API

### `loadingBar` Injection Methods

| 名称   | 类型         | 说明                     |
| ------ | ------------ | ------------------------ |
| error  | `() => void` | 加载条出现错误的回调函数 |
| finish | `() => void` | 加载条结束加载的回调函数 |
| start  | `() => void` | 加载条开始加载的回调函数 |
