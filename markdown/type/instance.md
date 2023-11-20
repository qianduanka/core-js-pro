## $core.instance

`$core.instance` 判断是否为当前实例。

#### 参数

- target 待判断的实例。
- objClass 类。

#### 返回值

返回布尔值，如果是对象是当前类的实例则返回真，否则，返回假。

### 例子

```javascript
let str = new String("qianduanka");
$core.instance(str, String); // true
$core.instance(str, Object); // false
```
