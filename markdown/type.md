## 类型

javascript 中包括基本类型和引用类型两大类，基本类型有 number、string、boolean、null、undefined、bigint、symbol。引用类型有 object。

## 方法

1. $core.type
2. $core.isPrimitive
3. $core.isNumber
4. $core.isString
5. $core.isBoolean
6. $core.isNull
7. $core.isUndefined
8. $core.isBigInt
9. $core.isSymbol
10. $core.isPureObject
11. $core.isObject
12. $core.isArray
13. $core.isNaN
14. $core.isFinite
15. $core.isFunction
16. $core.instance
17. $core.instanceof
18. $core.getClassName
19. $core.getClass
20. $core.isSet
21. $core.isMap
22. $core.isWeakSet
23. $core.isWeakMap
24. $core.isPromise
25. $core.isArrayBuffer
26. $core.isDataView
27. $core.isInt8Array
28. $core.isInt16Array
29. $core.isInt32Array
30. $core.isUint8Array
31. $core.isUint16Array
32. $core.isUint32Array
33. $core.isFloat32Array
34. $core.isFloat64Array
35. $core.isBigInt64Array
36. $core.isBigUint64Array

## $core.type 获取类型

### 语法

> $core.type(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回字符串，字符串表达类型的描述。

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

---

## $core.isPrimitive 判断是否为基本类型

### 语法

> $core.isPrimitive(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是基本类型返回真，否则，返回假。

### 例子

```javascript
$core.isPrimitive(521); // true
$core.isPrimitive("qianduanka"); // true
$core.isPrimitive(true); // true
$core.isPrimitive(null); // true
$core.isPrimitive(undefined); // true
$core.isPrimitive(521n); // true
$core.isPrimitive(Symbol("qdk")); // true

$core.isPrimitive([]); // false
$core.isPrimitive({}); // false
```

---

## $core.isNumber 判断是否为数值

### 语法

> $core.isNumber(target, isPrimitive = false)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是数值返回真，否则，返回假。

### 例子

```javascript
$core.isNumber(521); // true
$core.isNumber(Number(521)); // true
$core.isNumber(new Number(521)); // true

$core.isNumber(521, true); // true
$core.isNumber(Number(521), true); // true
$core.isNumber(new Number(521), true); // false
```

---

## $core.isString 判断是否为字符串

### 语法

> $core.isString(target, isPrimitive = false)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是字符串返回真，否则，返回假。

### 例子

```javascript
$core.isString("qianduanka"); // true
$core.isString(String("qianduanka")); // true
$core.isString(new String("qianduanka")); // true

$core.isString("qianduanka", true); // true
$core.isString(String("qianduanka"), true); // true
$core.isString(new String("qianduanka"), true); // false
```

---

## $core.isBoolean 判断是否为布尔值

### 语法

> $core.isBoolean(target, isPrimitive = false)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是布尔值返回真，否则，返回假。

### 例子

```javascript
$core.isBoolean(true); // true
$core.isBoolean(Boolean(true)); // true
$core.isBoolean(new Boolean(true)); // true

$core.isBoolean(true, true); // true
$core.isBoolean(Boolean(true), true); // true
$core.isBoolean(new Boolean(true), true); // false
```

---

## $core.isNull 判断是否为 null

### 语法

> $core.isNull(target)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是 null 返回真，否则，返回假。

### 例子

```javascript
$core.isNull(null); // true
```

---

## $core.isUndefined 判断是否为 undefined

### 语法

> $core.isUndefined(target)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是 null 返回真，否则，返回假。

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

---

## $core.isBigInt 判断是否为大整数

### 语法

> $core.isBigInt(target)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是字符串返回真，否则，返回假。

### 例子

```javascript
$core.isBigInt(521n); // true
$core.isBigInt(BigInt(521)); // true
```

---

## $core.isSymbol 判断是否为标识符

### 语法

> $core.isSymbol(target)

#### 参数

- target 待判断的值。
- isPrimitive 是否为原始值

#### 返回值

返回布尔值，如果是字符串返回真，否则，返回假。

### 例子

```javascript
$core.isSymbol(Symbol("qdk")); // true
$core.isSymbol(Symbol.for("qianduanka")); // true
```

---

## $core.isPureObject 判断是否为对象结构

### 语法

> $core.isPureObject(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是对象结构返回真，否则，返回假。

### 例子

```javascript
$core.isPureObject({}); // true
$core.isPureObject({ name: "qianduanka" }); // true
$core.isPureObject([]); // false
$core.isPureObject("qianduanka"); // false
$core.isPureObject(new String("qianduanka")); // false
$core.isPureObject(new Map()); // false
```

---

## $core.isObject 判断是否为对象

与 typeof 作用相同

### 语法

> $core.isObject(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是对象返回真，否则，返回假。

### 例子

```javascript
$core.isObject({}); // true
$core.isObject({ name: "qianduanka" }); // true
$core.isObject([]); // true
$core.isObject("qianduanka"); // false
$core.isObject(new String("qianduanka")); // true
$core.isObject(new Map()); // true
$core.isObject(null); // false

$core.isObject({}, true); // true
$core.isObject({ name: "qianduanka" }, true); // true
$core.isObject([]); // false
$core.isObject("qianduanka", true); // false
$core.isObject(new String("qianduanka"), true); // false
$core.isObject(new Map(), true); // false
$core.isObject(null, true); // false
```

## $core.isArray 判断是否为数组

与 Array.isArray 作用一样

### 语法

> $core.isArray(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是数组返回真，否则，返回假。

### 例子

```javascript
$core.isArray([]); // true
$core.isArray([521]); // true
$core.isArray(new Array()); // true
$core.isArray({}); // false
```

## 判断是否为 NaN

与 全局 Number.isNaN 作用一样

### 语法

> $core.isNaN(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是 NaN 返回真，否则，返回假。

### 例子

```javascript
$core.isNaN(NaN); // true
$core.isNaN("qdk"); // false
$core.isNan(521); // false
```

## $core.isFinite 判断是否为有限数值

与 全局 isFinite 作用一样

### 语法

> $core.isFinite(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是有限数值返回真，否则，返回假。

### 例子

```javascript
$core.isFinite(Infinity); // false
$core.isFinite(521); // true
```

## $core.isFunction 判断是否为方法

### 语法

> $core.isFunction(target)

#### 参数

- target 可以是任何类型的值。

#### 返回值

返回布尔值，如果是函数返回真，否则，返回假。

### 例子

```javascript
$core.isFunction(521); // false
$core.isFunction(new Number(521)); // false
$core.isFunction(Number); // true
$core.isFunction(() => {}); // true
$core.isFunction(function () {}); // true
$core.isFunction(class Book {}); // true
```

## $core.instance 判断是否为当前实例

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

---

## $core.instanceof 判断是否为当前实例

与 全局 instanceof 作用一样

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

---

## $core.getClassName 获取类名称

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

---

## $core.getClass 获取类

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

## $core.isSet 判断是否为 Set 的实例

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

## $core.isMap 判断是否为 Map 的实例

### 语法

> $core.isMap(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 Map 实例返回真，否则，返回假。

## 例子

```javascript
$core.isMap(new Map()); // true
$core.isMap([]); // false
$core.isMap({}); // false
```

## $core.isWeakSet 判断是否为 WeakSet 的实例

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

## $core.isWeakMap 判断是否为 WeakMap 的实例

### 语法

> $core.isWeakMap(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 WeakMap 实例返回真，否则，返回假。

## 例子

```javascript
$core.isWeakMap(new WeakMap()); // true
$core.isWeakMap([]); // false
$core.isWeakMap({}); // false
```

## $core.isPromise 判断是否为 Promise 的实例

### 语法

> $core.isPromise(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 Promise 实例返回真，否则，返回假。

## 例子

```javascript
$core.isPromise(new Promise(() => {})); // true
$core.isPromise(Promise.resolve("qianduanka")); // true
$core.isPromise(Promise); // false
```

## $core.isArrayBuffer 判断是否为 ArrayBuffer 的实例

### 语法

> $core.isArrayBuffer(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 ArrayBuffer 实例返回真，否则，返回假。

## 例子

```javascript
$core.isArrayBuffer(new ArrayBuffer(8)); // true
```

---

## $core.isDataView 判断是否为 DataView 的实例

### 语法

> $core.isDataView(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 ArrayBuffer 实例返回真，否则，返回假。

## 例子

```javascript
const buffer = new ArrayBuffer(8);
const dataview = new DataView(buffer);
$core.isDataView(dataview); // true
```

---

## $core.isInt8Array 判断是否为 DataView 的实例

### 语法

> $core.isInt8Array(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 ArrayBuffer 实例返回真，否则，返回假。

## 例子

### 例一、

```javascript
$core.isInt8Array(new Int8Array(8));

$core.isInt8Array(new Int8Array([21, 31]));
```

### 例二、

```javascript
const iterable = (function* () {
  yield* [1, 2, 3];
})();
const int8FromIterable = new Int8Array(iterable);
$core.isInt8Array(int8FromIterable); // true
```

### 例三、

```javascript
const buffer = new ArrayBuffer(8);
var int8Array = new Int8Array(buffer, 1, 4);
$core.isInt8Array(int8Array); // true
```

---

## $core.isUint8Array 判断是否为 DataView 的实例

### 语法

> $core.isUint8Array(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 ArrayBuffer 实例返回真，否则，返回假。

## 例子

### 例一、

```javascript
$core.isUint8Array(new Uint8Array());
$core.isUint8Array(new Uint8Array(8));
$core.isUint8Array(new Uint8Array([21, 31]));
```

### 例二、

```javascript
const iterable = (function* () {
  yield* [1, 2, 3];
})();
const uint8FromIterable = new Uint8Array(iterable);
$core.isUint8Array(uint8FromIterable); // true
```

### 例三、

```javascript
const buffer = new ArrayBuffer(8);
var uint8Array = new Uint8Array(buffer, 1, 4);
$core.isUint8Array(uint8Array); // true
```

---

## 同理

$core.isInt16Array、$core.isInt32Array、$core.isUint16Array、$core.isUint32Array、$core.isFloat32Array、$core.isFloat64Array、$core.isBigInt64Array、$core.isBigUint64Array 效果同 $core.isInt8Array、$core.isUint8Array
