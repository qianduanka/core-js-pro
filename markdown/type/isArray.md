## $core.isArray
`$core.isArray` 方法用于判断值是否为数组。与 Array.isArray 作用一样。

### 语法

> $core.isArray(target)

#### 参数

- target 待判断数组的值。

#### 返回值

返回布尔值，如果值是数组返回真，否则，返回假。

### 例子

```javascript
$core.isArray([]); // true
$core.isArray([521]); // true
$core.isArray(new Array()); // true
$core.isArray({}); // false
```