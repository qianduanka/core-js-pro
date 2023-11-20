# Collection 集合

## 方法

1. $core.size 长度或数量

## $core.size 深拷贝

### 语法

> $core.size(target)

#### 参数

- target 待统计的值

#### 返回值

返回数值，表示当前值的长度或数量。

### 例子

#### 例一、

```javascript
$core.size(); // 0
$core.size([]); // 0
$core.size("qianduanka"); // 10
$core.size("qianduanka前端咖"); // 13
$core.size("qianduanka前端咖", true); // 16
$core.size(new Set([1, 3, 5, 7, 9])); // 5
$core.size(new Map()); // 0
```
