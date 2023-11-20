# $core.sub

`$core.sub` 两个数相减。

## 语法

> $core.sub(minuend, subtrahend = undefined)

### 参数

- minuend 相减的第一个数。
- subtrahend 相减的第二个数。

### 返回值

返回两数相减的差。

## 例子

```javascript
$core.sub(3 - 2); // 1
$core.sub(3 - 2n); // 1
$core.sub(3n - 2n); // 1n
$core.sub(0.3 - 0.2); // 0.1
```
