## $core.isUndefined

`$core.isUndefined`方法用于判断值是否为 undefined 类型。

### 语法

> $core.isUndefined(target)

#### 参数

- target 待判断 undefined 类型的值。

#### 返回值

返回布尔值，如果值是 undefined 类型 返回真，否则，返回假。

### 例子

#### 例一、

```javascript
$core.isUndefined(undefined); // true
```

#### 例二、

```javascript
let obj = {};
$core.isUndefined(obj.name); // true
```
