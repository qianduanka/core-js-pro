## $core.isSet
`$core.isSet` 判断是否为 Set 的实例

### 语法

> $core.isSet(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 Set 实例返回真，否则，返回假。

## 例子

```javascript
$core.isSet(new Set()); // true
$core.isSet([]); // false
$core.isSet({}); // false
```