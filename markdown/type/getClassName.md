## $core.getClassName

`$core.getClassName` 获取类名称

### 语法

> $core.getClassName(target)

#### 参数

- target 实例。

#### 返回值

返回字符串，获取当前实例的类名称。如果不存在则返回 undefined。

### 例子

```javascript
let str = new String("qianduanka");
$core.getClassName(str); // String
```
