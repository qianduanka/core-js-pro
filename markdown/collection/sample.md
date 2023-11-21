# $core.sample

`$core.sample`方法用于随机获取数组中的元素。

## 语法

> $core.sample(collection = [], size)

### 参数

- collection 待获取元素的集合。

- size 可选 表示获取元素的个数。

### 返回值

返回元素或者数组，表示如果 size 有值时，将返回数组，否则，返回一个元素。

## 例子

### 例一、

```javascript
$core.sample(); // undefined
$core.sample([]); // undefined
$core.sample([1, 3, 5, 7, 9]); // 5 参考：仅表示当次运行的返回值。
$core.sample([1, 3, 5, 7, 9], 1); // [9] 参考：仅表示当次运行的返回值。
$core.sample(['a', 'b', 'c', 'd', 'e'], 3); // ["d","c","e"] 参考：仅表示当次运行的返回值。
```

### 例二、

```javascript
let users = [
  { user: '张三', age: 50 },
  { user: '李四', age: 36 },
  { user: '王五', age: 40 },
  { user: '赵六', age: 34 },
  { user: '孙七', age: 34 },
];

$core.sample(users); // {user:"王五",age:40} 参考：仅表示当次运行的返回值。
$core.sample(users, 3); // [{user:"张三",age:48},{user:"李四",age:36},{user:"王五",age:40}] 参考：仅表示当次运行的返回值。
```

### 例三、

```javascript
$core.sample('abcdef'); // a 参考：仅表示当次运行的返回值。
$core.sample('abcdef', 3); // ['a', 'e', 'f'] 参考：仅表示当次运行的返回值。
```

### 例四、

```javascript
$core.sample({
  a: 'aaa',
  b: 'bbb',
  c: 'ccc',
  d: 'ddd',
  e: 'eee',
}); // 'ccc' 参考：仅表示当次运行的返回值。

$core.sample(
  {
    a: 'aaa',
    b: 'bbb',
    c: 'ccc',
    d: 'ddd',
    e: 'eee',
  },
  3
); // ['ccc', 'aaa', 'ddd'] 参考：仅表示当次运行的返回值。
```

### 例五、

```javascript
$core.sample(new Set(['a', 'b', 'c', 'd', 'e'])); // 'e' 参考：仅表示当次运行的返回值。
$core.sample(new Set(['a', 'b', 'c', 'd', 'e']), 3); // ['e', 'b', 'c'] 参考：仅表示当次运行的返回值。
```

### 例六、

```javascript
$core.sample(
  new Map([
    ['a', 'aaa'],
    ['b', 'bbb'],
    ['c', 'ccc'],
    ['d', 'ddd'],
    ['e', 'eee'],
  ])
); // 'eee' 参考：仅表示当次运行的返回值。

$core.sample(
  new Map([
    ['a', 'aaa'],
    ['b', 'bbb'],
    ['c', 'ccc'],
    ['d', 'ddd'],
    ['e', 'eee'],
  ]),
  3
); // ['eee', 'ccc', 'aaa'] 参考：仅表示当次运行的返回值。
```

## 安装

```shell
npm install --save core-js-pro
```

## 使用

```javascript
import $core from 'core-js-pro';
```
