负责人：王硕

## NavigationBar
顶栏模块

### 基本用法

- `NavigationBar`作为容器与`NavigationBarItem`成对使用

```html
<navigation-bar :title="title">
  <navigation-bar-item slot="left" text="返回" icon="back" disable/>
  <navigation-bar-item slot="right" icon="search"  right-icon/>
</navigation-bar>
```
```js
import { NavigationBar, NavigationBarItem } from '@/components/NavigationBar'
export default {
  components: {
    NavigationBar,
    NavigationBarItem
  },
  data () {
    return {
      title: '我是标题党'
    }
  }
}
```
### NavigationBar Attributes

|参数|说明|类型|可选值|默认值|
|:-----|:-----|:-----|:-----|:-----|
|title|标题文字|`String`|-|`''`|
|sub-title|副标题文字|`String`|-|`''`|

### NavigationBar Slots

|name|说明|
|:-----|:-----|
|-|容纳自定义的顶栏布局，设置后其他`slot`、`title`和`sub-title`失效|
|left|左侧的`NavigationBarItem`|
|right|右侧的`NavigationBarItem`|

### BottomBarItem Attributes

|参数|说明|类型|可选值|默认值|
|:-----|:-----|:-----|:-----|:-----|
|name|显示的文字|String|-|`bottom-bar-item`|
|icon|图标的名称|String|`@/components/Icon/svg/`中的`SVG`文件名|-|
|active|激活状态|Boolean|`true`、`false`|`false`|
|disable|设为不可用|Boolean|`true`、`false`|`false`|
