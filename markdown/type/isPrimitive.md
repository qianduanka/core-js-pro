## $core.isPrimitive

`$core.isPrimitive`方法用于判断值是否为基本类型。

### 语法

> $core.isPrimitive(target)

#### 参数

- target 待判断基本类型的值。

#### 返回值

返回布尔值，如果值是基本类型返回真，否则，返回假。

### 例子

```javascript
$core.isPrimitive(521); // true
$core.isPrimitive("qianduanka"); // true
$core.isPrimitive(true); // true
$core.isPrimitive(null); // true
$core.isPrimitive(undefined); // true
$core.isPrimitive(521n); // true
$core.isPrimitive(Symbol("qdk")); // true
$core.isPrimitive(Number(521)); // true
$core.isPrimitive(String("qianduanka")); // true

$core.isPrimitive(new Number(521)); // false
$core.isPrimitive(new String("qianduanka")); // false
$core.isPrimitive([]); // false
$core.isPrimitive({}); // false
```
