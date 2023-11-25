# $core.ceil

`$core.ceil`方法用于按照指定精度向上舍入。

## 语法

> $core.ceil(number, precision = 0)

### 参数

- number 数值。
- precision 指定精度，默认为 0。

### 返回值

返回数值或大整数类型。

## 例子

### 例一、

```javascript
$core.ceil(3.141592653589793); // 4
$core.ceil(2.718281828459045); // 3
```

## 例二、

```javascript
$core.ceil(3.141592653589793, 2); // 3.15
$core.ceil(2.718281828459045, 2); // 2.72
```

## 例二、

```javascript
$core.ceil(314159.2653589793, -2); // 314200
$core.ceil(271828.1828459045, -2); // 271900
```
