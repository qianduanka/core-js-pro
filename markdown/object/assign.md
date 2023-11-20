# $core.assign

`$core.assign` 扩展

## 语法

> let target = $core.assign(target, source);
> let target = $core.assign(target, source1, ... , sourceN);

### 参数

- target 需要应用源对象属性的目标对象，修改后将作为返回值。
- source 一个或多个包含要应用的属性的源对象。

### 返回值

修改后的目标对象。

## 例子

### 例一、

```javascript
let obj = {};
$core.assign(obj, { name: "qianduanka" });
console.log(obj); // { "name": "qianduanka" }

let arr = [];
$core.assign(arr, [1, 3, 5, 7, 9]);
console.log(arr); // [1, 3, 5, 7, 9]
```

### 例二、

```javascript
let obj = { name: "qianduanka", arr: [1, 3, 5, 7, 9] };
$core.assign(obj, { arr: [6, 8], age: 23 }, { name: "qdk" });
console.log(obj); // { "name": "qdk", "arr": [ 6, 8 ], "age": 23 }
```


### 例三、

```javascript
let arr = [
  { name: "a", age: 3 },
  { name: "b", age: 1 },
  { name: "c", age: 9 },
  { name: "d", age: 5 },
  { name: "e", age: 7 },
];
$core.assign(arr, [{ age: 6 }, { age: 8 }]);
console.log(arr);

/*
[
    {
        "age": 6
    },
    {
        "age": 8
    },
    {
        "name": "c",
        "age": 9
    },
    {
        "name": "d",
        "age": 5
    },
    {
        "name": "e",
        "age": 7
    }
]
*/
```