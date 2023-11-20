# $core.insertString

`$core.insertString` 方法用于插入从索引位置的字符串。

## 语法

> $core.insertString(string = '', start = 0, ...args)

### 参数

- string 参数待转换成字符串。
- start 插入的索引位置。
- args 将插入的字符串。

### 返回值

返回删除后的新字符串。

## 例子

```javascript
$core.insertString("qianduanka"); // 'qianduanka'
$core.insertString("qianduanka", 3, 5, "*****"); // 'qianduanka'
$core.insertString("qianduanka", -6, 3, "***"); // 'qian123duanka'
```
