## $core.isInt8Array

`$core.isInt8Array` 判断是否为 DataView 的实例

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


## 同理

$core.isInt16Array、$core.isInt32Array、$core.isUint16Array、$core.isUint32Array、$core.isFloat32Array、$core.isFloat64Array、$core.isBigInt64Array、$core.isBigUint64Array 效果同 $core.isInt8Array、$core.isUint8Array