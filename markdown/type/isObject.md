# $core.isObject

`$core.isObject` 方法用于判断值是否为对象。

## 语法

> $core.isObject(target, primitive)

### 参数

- target 待判断对象的值。
- primitive 是否为原始基本类型。

### 返回值

返回布尔值，如果值是对象返回真，否则，返回假。

## 例子

### 例一、

```javascript
$core.isObject({}); // true
$core.isObject({ name: "qianduanka" }); // true
$core.isObject([]); // true
$core.isObject("qianduanka"); // false
$core.isObject(new String("qianduanka")); // true
$core.isObject(new Map()); // true
$core.isObject(null); // false
```

### 例二、

```javascript
$core.isObject({}, $core.PRIMITIVE); // true
$core.isObject({ name: "qianduanka" }, $core.PRIMITIVE); // true
$core.isObject([], $core.PRIMITIVE); // false
$core.isObject("qianduanka", $core.PRIMITIVE); // false
$core.isObject(new String("qianduanka"), $core.PRIMITIVE); // false
$core.isObject(new Map(), $core.PRIMITIVE); // false
$core.isObject(null, $core.PRIMITIVE); // false
```
