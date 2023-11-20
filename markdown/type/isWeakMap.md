
## $core.isWeakMap
`$core.isWeakMap` 判断是否为 WeakMap 的实例

### 语法

> $core.isWeakMap(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 WeakMap 实例返回真，否则，返回假。

## 例子

```javascript
$core.isWeakMap(new WeakMap()); // true
$core.isWeakMap([]); // false
$core.isWeakMap({}); // false
```