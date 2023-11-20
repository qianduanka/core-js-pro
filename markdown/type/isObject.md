## $core.isObject 判断是否为对象

`$core.isObject` 方法用于判断值是否为对象。

与 typeof 作用相同

### 语法

> $core.isObject(target)

#### 参数

- target 待判断对象的值。

#### 返回值

返回布尔值，如果值是对象返回真，否则，返回假。

### 例子

```javascript
$core.isObject({}); // true
$core.isObject({ name: "qianduanka" }); // true
$core.isObject([]); // true
$core.isObject("qianduanka"); // false
$core.isObject(new String("qianduanka")); // true
$core.isObject(new Map()); // true
$core.isObject(null); // false

$core.isObject({}, true); // true
$core.isObject({ name: "qianduanka" }, true); // true
$core.isObject([]); // false
$core.isObject("qianduanka", true); // false
$core.isObject(new String("qianduanka"), true); // false
$core.isObject(new Map(), true); // false
$core.isObject(null, true); // false
```
