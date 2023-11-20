## $core.upperFirst
`$core.upperFirst` 方法用于将参数转换成字符串。

### 语法

> $core.upperFirst(target = '')

#### 参数

- target 参数待转换成字符串。

#### 返回值

返回字符串，默认返回空字符串。

### 例子

```javascript
$core.upperFirst(); // ''
$core.upperFirst(null); // ''
$core.upperFirst(undefined); // ''
$core.upperFirst(521); // 521
$core.upperFirst(521n); // 521
$core.upperFirst(true); // 'True'
```