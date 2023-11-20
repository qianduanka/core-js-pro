# $core.reduceTarget

`$core.reduceTarget` 继承

## 语法

> $core.reduceTarget(target, descTarget);

### 参数

- target 待精简化对象
- descTarget 精简化描述结构

### 返回值

返回精简化后的新对象。

## 例子

### 例一、

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

### 例二、

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

### 例三、

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
