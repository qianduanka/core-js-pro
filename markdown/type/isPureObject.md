
## $core.isPureObject
`$core.isPureObject`方法用于判断值是否为对象结构。

### 语法

> $core.isPureObject(target)

#### 参数

- target 待判断对象结构的值。

#### 返回值

返回布尔值，如果值是对象结构返回真，否则，返回假。

### 例子

```javascript
$core.isPureObject({}); // true
$core.isPureObject({ name: "qianduanka" }); // true
$core.isPureObject([]); // false
$core.isPureObject("qianduanka"); // false
$core.isPureObject(new String("qianduanka")); // false
$core.isPureObject(new Map()); // false
$core.isPureObject(null); // false
```