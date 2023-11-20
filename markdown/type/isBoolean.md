## $core.isBoolean

`$core.isBoolean`方法用于判断值是否为布尔类型。

### 语法

> $core.isBoolean(target, primitive)

#### 参数

- target 待判断布尔类型的值。
- primitive 默认 undefined，如果是 $core.PRIMITIVE 值，标记为原始类型。

#### 返回值

返回布尔值，如果值是布尔类型返回真，否则，返回假。

### 例子

```javascript
$core.isBoolean(true); // true
$core.isBoolean(Boolean(true)); // true
$core.isBoolean(new Boolean(true)); // true

$core.isBoolean(true, $core.PRIMITIVE); // true
$core.isBoolean(Boolean(true), $core.PRIMITIVE); // true
$core.isBoolean(new Boolean(true), $core.PRIMITIVE); // false
```