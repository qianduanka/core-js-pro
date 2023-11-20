## $core.isUint8Array

`$core.isUint8Array` 判断是否为 DataView 的实例

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

## 同理

$core.isInt16Array、$core.isInt32Array、$core.isUint16Array、$core.isUint32Array、$core.isFloat32Array、$core.isFloat64Array、$core.isBigInt64Array、$core.isBigUint64Array 效果同 $core.isInt8Array、$core.isUint8Array
