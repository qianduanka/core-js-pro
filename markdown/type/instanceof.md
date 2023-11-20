## $core.instanceof

`$core.instanceof` 判断是否为当前实例。与 全局 instanceof 作用一样。

#### 参数

- target 待判断的实例。
- objClass 类。

#### 返回值

返回布尔值，如果是对象是类或类原型链上的实例则返回真，否则，返回假。

### 例子

```javascript
let str = new String("qianduanka");
$core.instanceof(str, String); // true
$core.instanceof(str, Object); // true
```
