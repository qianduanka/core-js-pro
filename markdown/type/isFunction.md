## $core.isFunction
`$core.isFunction`方法用于判断值是否为函数。

### 语法

> $core.isFunction(target)

#### 参数

- target 待判断函数的参数。

#### 返回值

返回布尔值，如果是函数返回真，否则，返回假。

### 例子

```javascript
$core.isFunction(521); // false
$core.isFunction(new Number(521)); // false
$core.isFunction(Number); // true
$core.isFunction(() => {}); // true
$core.isFunction(function () {}); // true
$core.isFunction(class Book {}); // true
```