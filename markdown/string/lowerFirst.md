## $core.lowerFirst
`$core.lowerFirst` 方法用于将参数转换成字符串。

### 语法

> $core.lowerFirst(target = '')

#### 参数

- target 参数待转换成字符串。

#### 返回值

返回字符串，默认返回空字符串。

### 例子

```javascript
$core.lowerFirst(); // ''
$core.lowerFirst(null); // ''
$core.lowerFirst(undefined); // ''
$core.lowerFirst(521); // 521
$core.lowerFirst(521n); // 521
$core.lowerFirst(true); // 'true'
```