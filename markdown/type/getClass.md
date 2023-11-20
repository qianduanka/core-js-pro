## $core.getClass
`$core.getClass` 获取类

### 语法

> $core.getClass(target)

#### 参数

- target 实例。

#### 返回值

返回类，获取当前实例的类。如果不存在则返回 undefined。

### 例子

```javascript
let str = new String("qianduanka");
$core.getClass(str);
```