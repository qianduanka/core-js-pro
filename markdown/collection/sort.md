# $core.sort

`$core.sort`方法用于将数组元素进行排序，并返回排序后的数组。

## 语法

> $core.sort(target = [])
>
> $core.sort(target = [], order)
>
> $core.sort(target = [], [iteratee, order])
>
> $core.sort(target = [], [iteratee, order] , ... , [iterateeN, order])
>
> $core.sort(target = [], [iteratee, order, locale] , ... , [iterateeN, order, locale])

### 参数

- target 待排序的数组。
- iteratee 可选 字符串或者函数。
- order 可选 顺序，默认升序。 $core.ASC 升序， $core.DESC 降序。
- locale 可选 用本地比对排序。

### 返回值

返回对象，表示一个组成聚合对象。

## 描述

target 指待排序的数组。

1. iteratee 当为字符串时，表示按照元素的属性值比较进行排序。

2. iteratee 当为函数时，表示按照元素的函数返回值比较进行排序。

## 例子

### 例一、

```javascript
$core.sort(); // []
$core.sort([]); // []
$core.sort([3, 1, 9, 5, 7], $core.DESC); // [9, 7, 5, 3, 1]
```

### 例二、

```javascript
let users = [
  { user: "张三", age: 50 },
  { user: "李四", age: 36 },
  { user: "王五", age: 40 },
  { user: "赵六", age: 34 },
  { user: "孙七", age: 34 },
];

$core.sort(users, ["age", $core.ASC]);

/*
[
  {
    user: '赵六',
    age: 34,
  },
  {
    user: '孙七',
    age: 34,
  },
  {
    user: '李四',
    age: 36,
  },
  {
    user: '王五',
    age: 40,
  },
  {
    user: '张三',
    age: 50,
  },
]
 */
```

### 例三、

```javascript
let users = [
  { user: "张三", age: 50 },
  { user: "李四", age: 36 },
  { user: "王五", age: 40 },
  { user: "赵六", age: 34 },
  { user: "孙七", age: 34 },
];

$core.sort(users, ["user", $core.ASC, $core.LOCALE]);

/*
[
  {
    user: '李四',
    age: 36,
  },
  {
    user: '孙七',
    age: 34,
  },
  {
    user: '王五',
    age: 40,
  },
  {
    user: '张三',
    age: 50,
  },
  {
    user: '赵六',
    age: 34,
  },
]
*/
```

### 李四、

```javascript
let usersC = [
  { user: "张三", age: 50 },
  { user: "李四", age: 36 },
  { user: "王五", age: 40 },
  { user: "赵六", age: 34 },
  { user: "孙七", age: 34 },
];

$core.sort(usersC, ["age", $core.ASC], ["user", $core.DESC, $core.LOCALE]);

/*
[
  {
    user: '赵六',
    age: 34,
  },
  {
    user: '孙七',
    age: 34,
  },
  {
    user: '李四',
    age: 36,
  },
  {
    user: '王五',
    age: 40,
  },
  {
    user: '张三',
    age: 50,
  },
]
*/
```
