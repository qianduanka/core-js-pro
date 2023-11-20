# $core.cloneDeep

`$core.cloneDeep` 深拷贝

## 语法

> let newTarget = $core.cloneDeep(target)

### 参数

- target 待拷贝的对象。

### 返回值

返回对象。

## 例子

### 例一、

```javascript
let obj = {};
let newObj = $core.deepCopy(obj);
console.log(newObj);

let arr = [];
let newArr = $core.deepCopy(arr);
console.log(newArr);
```

### 例二、

```javascript
let obj = { name: "qianduanka", arr: [1, 3, 5, 7, 9] };
let newObj = $core.deepCopy(obj);
console.log(newObj);

let arr = [
  { name: "a", age: 3 },
  { name: "b", age: 1 },
  { name: "c", age: 9 },
  { name: "d", age: 5 },
  { name: "e", age: 7 },
];
let newArr = $core.deepCopy(arr);
console.log(newArr);
```
