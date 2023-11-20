# $core.add

`$core.add` 两个数相加。

## 语法

> $core.add(augend, addend = undefined)

### 参数

- augend 相加的第一个数。
- addend 相加的第二个数。

### 返回值

返回两数相加的和。

## 例子

```javascript
$core.add(1 + 2); // 3
$core.add(1 + 2n); // 3
$core.add(1n + 2n); // 3n
$core.add(0.1 + 0.2); // 0.3
```
