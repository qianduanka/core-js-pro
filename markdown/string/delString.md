# $core.delString

`$core.delString` 方法用于删除从索引位置指定长度字符。

## 语法

> $core.delString(string = '', start = 0, deleteCount = string.length)

### 参数

- string 参数待转换成字符串。
- start 插入的索引位置。
- deleteCount 删除字符串的长度，默认删除到末尾。

### 返回值

返回删除后的新字符串。

## 例子

```javascript
$core.delString("qianduanka"); // 'qianduanka'
$core.delString("qianduanka", 3); // 'qia'
$core.delString("qianduanka", 3, 1); // 'qiaduanka'
$core.delString("qianduanka", -3, 1); // 'qianduaka'
$core.delString("qianduanka", -3); // 'qiandua'
```
