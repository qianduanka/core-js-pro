## $core.isNumber

`$core.isNumber`方法用于判断参数是否为数值类型。

### 语法

> $core.isNumber(target, primitive)

#### 参数

- target 待判断参数为数值类型。
- primitive 默认 undefined，如果参数是 $core.PRIMITIVE，标记为原始类型。

#### 返回值

返回布尔值，如果参数是数值类型返回真，否则，返回假。

### 例子

```javascript
$core.isNumber(521); // true
$core.isNumber(Number(521)); // true
$core.isNumber(new Number(521)); // true

$core.isNumber(521, $core.PRIMITIVE); // true
$core.isNumber(Number(521), $core.PRIMITIVE); // true
$core.isNumber(new Number(521), $core.PRIMITIVE); // false
```
