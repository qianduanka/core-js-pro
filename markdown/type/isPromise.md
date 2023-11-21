## $core.isPromise
`$core.isPromise` 判断是否为 Promise 的实例

### 语法

> $core.isPromise(target)

#### 参数

- target 待判断的值。

#### 返回值

返回布尔值，如果是 Promise 实例返回真，否则，返回假。

## 例子

```javascript
$core.isPromise(new Promise(() => {})); // true
$core.isPromise(Promise.resolve('qianduanka')); // true
$core.isPromise(Promise.reject('qianduanka')); // true
$core.isPromise(Promise); // false
$core.isPromise(await function () {}); // false
```