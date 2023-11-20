# Object 对象

## 方法

1. $core.cloneDeep 深拷贝
2. $core.extend 继承
3. $core.equalTarget 判断对象键值对是否一样
4. $core.reduceTarget 结构精简化对象

## $core.cloneDeep 深拷贝

### 语法

> let newTarget = $core.cloneDeep(target)

#### 参数

- target 待拷贝的对象

#### 返回值

返回对象

### 例子

#### 例一、

```javascript
let obj = {};
let newObj = $core.deepCopy(obj);
console.log(newObj);

let arr = [];
let newArr = $core.deepCopy(arr);
console.log(newArr);
```

#### 例二、

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

---

## $core.extend 继承

### 语法

> let target = $core.extend(target, source);
> let target = $core.extend(target, source1, ... , sourceN);

#### 参数

- target 待拷贝的对象

#### 返回值

返回对象

### 例子

#### 例一、

```javascript
let obj = {};
$core.extend(obj, { name: "qianduanka" });
console.log(obj);

let arr = [];
$core.extend(arr, [1, 3, 5, 7, 9]);
console.log(arr);
```

#### 例二、

```javascript
let obj = { name: "qianduanka", arr: [1, 3, 5, 7, 9] };
$core.extend(obj, { arr: [6, 8], age: 23 }, { name: "qdk" });
console.log(obj);

let arr = [
  { name: "a", age: 3 },
  { name: "b", age: 1 },
  { name: "c", age: 9 },
  { name: "d", age: 5 },
  { name: "e", age: 7 },
];
$core.extend(arr, [{ age: 6 }, { age: 8 }]);
console.log(arr);
```

---

## $core.equalTarget 判断对象键值对是否一样

### 语法

> $core.equalTarget(targetA, targetB);

#### 参数

- targetA 待比较对象一
- targetB 待比较对象二

#### 返回值

返回对象

### 例子

#### 例一、

```javascript
$core.equalTarget({}, {}); // true
$core.equalTarget([], []); // true
```

#### 例二、

```javascript
$core.equalTarget({ name: "qianduanka" }, { name: "qianduanka" }); // true
$core.equalTarget([1, 3, 5, 7, 9], [1, 3, 5, 7, 9]); // true

$core.equalTarget(
  { name: "qianduanka", value: 3 / 0 },
  { name: "qianduanka", value: 5 / 0 }
); // true
$core.equalTarget([1, 3 / 0, 5, 7, 9], [1, 33 / 0, 5, 7, 9]); // true
```

#### 例三、

```javascript
console.log($core.equalTarget("qianduanka", "qianduanka")); // true
console.log($core.equalTarget(3 / 0, 5 / 0)); // true
```

---

## $core.reduceTarget 继承

### 语法

> $core.reduceTarget(target, descTarget);

#### 参数

- target 待精简化对象
- descTarget 精简化描述结构

#### 返回值

返回精简化后的新对象。

### 例子

#### 例一、

```javascript
$core.reduceTarget(
  { name: "qianduanka", age: 25 },
  {
    name: null,
    book: "JavaScript",
  }
);
// { "name": "qianduanka", "book": "JavaScript" }
```

#### 例二、

```javascript
$core.reduceTarget(
  [
    { name: "a", age: 3 },
    { name: "b", age: 1 },
    { name: "c", age: 9 },
    { name: "d", age: 5 },
    { name: "e", age: 7 },
  ],
  [
    {
      name: null,
    },
  ]
);

// [
//   {
//       "name": "a"
//   },
//   {
//       "name": "b"
//   },
//   {
//       "name": "c"
//   },
//   {
//       "name": "d"
//   },
//   {
//       "name": "e"
//   }
// ]
```

#### 例三、

```javascript
$core.reduceTarget(
  {
    name: "qianduanka",
    age: 25,
    list: [
      { id: 1, name: "a", age: 3 },
      { id: 2, name: "b", age: 1 },
      { id: 3, name: "c", age: 9 },
      { id: 4, name: "d", age: 5 },
      { id: 5, name: "e", age: 7 },
    ],
  },
  {
    name: null,
    from: "前端咖",
    list: [{ id: null }],
  }
);

// {
//   "name": "qianduanka",
//   "from": "前端咖",
//   "list": [
//     {
//       "id": 1
//     },
//     {
//       "id": 2
//     },
//     {
//       "id": 3
//     },
//     {
//       "id": 4
//     },
//     {
//       "id": 5
//     }
//   ]
// }
```
