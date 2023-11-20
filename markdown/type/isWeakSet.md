## $core.isWeakSet
`$core.isWeakSet` 判断是否为 WeakSet 的实例。

### 语法

> $core.isWeakSet(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 WeakSet 实例返回真，否则，返回假。

## 例子

```javascript
$core.isWeakSet(new WeakSet()); // true
$core.isWeakSet([]); // false
$core.isWeakSet({}); // false
```