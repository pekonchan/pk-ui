# popper 浮窗

## 代码演示

<script>
    export default {
        data () {
            return {
                value1: false,
                value2: true
            }
        }
    }
</script>

### 基础应用
::: demo
```html
<com-popper>
    <template v-slot:reference>悬浮显示浮窗</template>
    这是浮窗的内容
</com-popper>
```
:::

### 选择触发popper方式

::: demo
```html
<com-popper trigger="hover">
    <template v-slot:reference>悬浮显示浮窗</template>
    这是浮窗的内容
</com-popper>

<com-popper trigger="click">
    <template v-slot:reference>点击显示浮窗</template>
    这是浮窗的内容
</com-popper>
```
```js
<script>
    export default {
        data () {
            return {
                value2: true
            }
        }
    }
</script>
```
:::

### Props

| 参数 | 说明 | 类型 | 可选值 | 默认值 | 是否必填 |
| ---- | -------------- | ------ |------- | -------- | --- |
| placement | 浮窗的位置 | String | auto, auto-start, auto-end, top, top-start, top-end, bottom, bottom-start, bottom-end, right, right-start, right-end, left,  left-start, left-end | bottom | no |
| disabled | 是否禁用复选框 | Boolean | true/false | false | no |

### events
| 参数 | 说明 | 回调参数 |
| ---- | -------------- | ------ |
| change | 改变复选框值触发 | 新值 |