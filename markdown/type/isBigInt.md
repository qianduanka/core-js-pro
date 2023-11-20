## $core.isBigInt

`$core.isBigInt`方法用于判断值是否为大整数类型。

### 语法

> $core.isBigInt(target)

#### 参数

- target 待判断大整数类型的值。

#### 返回值

返回布尔值，如果值是大整数类型返回真，否则，返回假。

### 例子

```javascript
$core.isBigInt(521n); // true
$core.isBigInt(BigInt(521)); // true
```
