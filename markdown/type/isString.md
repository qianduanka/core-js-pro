## $core.isString

`$core.isString`方法用于判断值是否为字符串类型。

### 语法

> $core.isString(target, primitive)

#### 参数

- target 待判断字符串类型的值。
- primitive 默认 undefined，如果是 $core.PRIMITIVE 值，标记为原始类型。

#### 返回值

返回布尔值，如果值是字符串类型返回真，否则，返回假。

### 例子

```javascript
$core.isString("qianduanka"); // true
$core.isString(String("qianduanka")); // true
$core.isString(new String("qianduanka")); // true

$core.isString("qianduanka", $core.PRIMITIVE); // true
$core.isString(String("qianduanka"), $core.PRIMITIVE); // true
$core.isString(new String("qianduanka"), $core.PRIMITIVE); // false
```
