# $core.size

`$core.size`方法用于获取当前参数值的长度或数量。

## 语法

> $core.size(target, isChar = false)

### 参数

- target 待统计值长度或数量。

- isChar 只在当前值是字符串时有效，如果为true按照字节统计，一个汉字代表两个字节。

### 返回值

返回数值，表示当前值的长度或数量。

## 例子

### 例一、

```javascript
$core.size(); // 0
$core.size([]); // 0
$core.size([1, 3, 5, 7, 9]); // 5
$core.size(new Set(['a', 'b', 'c'])); // 3
$core.size(new Map()); // 0
$core.size({0: 'a', 1: 'b', 2: 'c', 3: 'd', length: 4}); // 4
$core.size('qianduanka'); //10
$core.size('qianduanka前端咖'); // 13
$core.size('qianduanka前端咖', true); // 16
```
