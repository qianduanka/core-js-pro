# $core.isEmpty

`$core.isEmpty`方法用于判断值是否为假值或者是空数组、空对象、类数组长度为0，空Set、空Map。

## 语法

> $core.isEmpty(target)

### 参数

- target 可以是任何类型的值。

### 返回值

返回布尔值，如果是参数是假值或者是空数组、空对象、类数组长度为0，空Set、空Map，返回真，否则，返回假。

## 例子

### 例一、

```javascript
$core.isEmpty(); // true
$core.isEmpty(undefined); // true
$core.isEmpty(null); // true
$core.isEmpty(""); // true
$core.isEmpty(0); // true
$core.isEmpty(0n); // true
$core.isEmpty(false); // true
$core.isEmpty([]); // true
$core.isEmpty({}); // true
$core.isEmpty(new Set()); // true
$core.isEmpty(new Map()); // true
```

### 例二、

```javascript
function demo() {
  console.log($core.isEmpty(arguments)); // true
}

demo();
```
