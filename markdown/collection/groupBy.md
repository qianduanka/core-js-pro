# $core.groupBy

`$core.groupBy`方法用于将数组按照指定的规则进项分组。

## 语法

> $core.groupBy(target = [], iteratee)

### 参数

- target 待分组的数组。
- iteratee 字符串或者函数。

### 返回值

返回对象，表示一个组成聚合对象。

## 描述

target 指待分组的数组。

1. iteratee 当为字符串时，表示按照元素的属性进行分组。

2. iteratee 当为函数时，表示按照元素的函数返回的规则进行分组。

## 例子

### 例一、

```javascript
$core.group(); // {}

$core.group($core.groupBy([3.14, 6.2, 3.3], Math.floor)); // {3:[3.14, 3.3],6:[6.2]}
$core.groupBy(["one", "two", "three"], "length"); // {3:["one","two"],5:["three"]}
$core.groupBy(["one", "two", "three"], (item) => item[0]); // {o:["one"],t:["two","three"]}
```

### 例二、

```javascript
$core.group("qianduanka");

/*
{
  q: ['q'],
  i: ['i'],
  a: ['a', 'a', 'a'],
  n: ['n', 'n'],
  d: ['d'],
  u: ['u'],
  k: ['k'],
}
*/
```

### 例三、

```javascript
$core.group($core.groupBy({ a: "aaa", b: "bbb", c: "ccc", aa: "aaa" }));

/*
{
  aaa: ['aaa', 'aaa'],
  bbb: ['bbb'],
  ccc: ['ccc'],
}
*/
```

### 例二、

```javascript
const inventory = [
  { name: "asparagus", type: "vegetables", quantity: 9 },
  { name: "bananas", type: "fruit", quantity: 5 },
  { name: "goat", type: "meat", quantity: 23 },
  { name: "cherries", type: "fruit", quantity: 12 },
  { name: "fish", type: "meat", quantity: 22 },
];
$core.groupBy(inventory, ({ type }) => type);

/*
{
  vegetables: [{ name: 'asparagus', type: 'vegetables', quantity: 9 }],
  fruit: [
    { name: 'bananas', type: 'fruit', quantity: 5 },
    { name: 'cherries', type: 'fruit', quantity: 12 },
  ],
  meat: [
    { name: 'goat', type: 'meat', quantity: 23 },
    { name: 'fish', type: 'meat', quantity: 22 },
  ],
}
*/
```

### 例三、

```javascript
const inventory = [
  { name: "asparagus", type: "vegetables", quantity: 9 },
  { name: "bananas", type: "fruit", quantity: 5 },
  { name: "goat", type: "meat", quantity: 23 },
  { name: "cherries", type: "fruit", quantity: 12 },
  { name: "fish", type: "meat", quantity: 22 },
];

const restock = { restock: true };
const sufficient = { restock: false };
const result = $core.groupBy(
  inventory,
  ({ quantity }) => (quantity < 6 ? restock : sufficient),
  $core.MAP
);

console.log(result.get(restock));

// [{ name: 'bananas', type: 'fruit', quantity: 5 }]
```
