## $core.isFinite

`$core.isFinite`方法用于判断值是否为有限数值。与 全局 isFinite 作用一样。

### 语法

> $core.isFinite(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是有限数值返回真，否则，返回假。

### 例子

```javascript
$core.isFinite(Infinity); // false
$core.isFinite(NaN); // false
$core.isFinite(); // false
$core.isFinite(undefined); // false
$core.isFinite(null); // true
$core.isFinite(521); // true
$core.isFinite(521n); // true 备注：大整数（BigInt）都是有限的整数
```
