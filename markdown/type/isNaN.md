## $core.isNaN

`$core.isNaN`方法用于判断值是否为 NaN。与 全局 Number.isNaN 作用一样。

### 语法

> $core.isNaN(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是 NaN 返回真，否则，返回假。

### 例子

```javascript
$core.isNaN(NaN); // true
$core.isNaN("qdk"); // false
$core.isNan(521); // false
```
