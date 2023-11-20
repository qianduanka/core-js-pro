## $core.type

`$core.type`方法用于获取值的类型。

### 语法

> $core.type(target)

#### 参数

- target 待获取类型的值。

#### 返回值

返回字符串，字符串表示类型的描述。

### 例子

#### 例一、基本类型

```javascript
$core.type(521); // 'number'
$core.type(new Number(521)); // 'number'
$core.type(NaN); // 'number'
$core.type(Infinity); // 'number'
$core.type(Math.PI); // 'number'
$core.type("qianduanka"); // 'string'
$core.type(new String("qianduanka")); // 'string'
$core.type(true); // 'boolean'
$core.type(new Boolean(true)); // 'boolean'
$core.type(null); // 'null'
$core.type(undefined); // 'undefined'
$core.type(521n); // 'bigint'
$core.type(BigInt(521)); // 'bigint'
$core.type(Symbol("qdk")); // 'symbol'
$core.type(Symbol.for("qdk")); // 'symbol'
```

#### 例二、引用类型

```javascript
$core.type([]); // 'array'
$core.type({}); // 'object'
$core.type(new Set()); // 'set'
$core.type(new Map()); // 'map'
$core.type(new WeakSet()); // 'weakset'
$core.type(new WeakMap()); // 'weakmap'
$core.type(new RegExp("qdk")); // 'regexp'
$core.type(/qdk/gi); // 'regexp'
$core.type(new Date()); // 'date'
$core.type(new Promise()); // 'promise'
$core.type(new Int16Array()); // 'int16array'
$core.type(new ArrayBuffer()); // 'arraybuffer'
$core.type(new DataView()); // 'dataview'
$core.type(new Proxy()); // 'proxy'
```
