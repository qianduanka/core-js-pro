## $core.isSymbol
`$core.isSymbol`方法用于判断值是否为标识符类型。

### 语法

> $core.isSymbol(target)

#### 参数

- target 待判断标识符类型的值。

#### 返回值

返回布尔值，如果值是标识符类型返回真，否则，返回假。

### 例子

```javascript
$core.isSymbol(Symbol("qdk")); // true
$core.isSymbol(Symbol.for("qianduanka")); // true
```