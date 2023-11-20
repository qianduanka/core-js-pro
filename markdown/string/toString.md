## $core.toString
`$core.toString` 方法用于将参数转换成字符串。

### 语法

> $core.toString(target)

#### 参数

- target 参数待转换成字符串。

#### 返回值

返回字符串，默认返回空字符串。

### 例子

```javascript
$core.toString(); // ''
$core.toString(null); // ''
$core.toString(undefined); // ''
$core.toString(521); // 521
$core.toString(521n); // 521
$core.toString(true); // 'true'
```