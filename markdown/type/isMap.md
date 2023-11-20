## $core.isMap

`$core.isMap` 判断是否为 Map 的实例。

### 语法

> $core.isMap(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 Map 实例返回真，否则，返回假。

## 例子

```javascript
$core.isMap(new Map()); // true
$core.isMap([]); // false
$core.isMap({}); // false
```
