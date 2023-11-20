## $core.isDataView

`$core.isDataView` 判断是否为 DataView 的实例

### 语法

> $core.isDataView(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 ArrayBuffer 实例返回真，否则，返回假。

## 例子

```javascript
const buffer = new ArrayBuffer(8);
const dataview = new DataView(buffer);
$core.isDataView(dataview); // true
```
