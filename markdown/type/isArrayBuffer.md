
## $core.isArrayBuffer
`$core.isArrayBuffer` 判断是否为 ArrayBuffer 的实例

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