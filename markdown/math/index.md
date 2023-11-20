# MATH 数学

## 方法

1. $core.add 加法
2. $core.sub 减法
3. $core.mul 乘法
4. $core.div 除法
5. $core.min 最小值
6. $core.max 最大值
7. $core.sum 求和
8. $core.mean 平均值
9. $core.floor 按精度向下
10. $core.ceil 按精度向上
11. $core.round 按精度四舍五入

## $core.add 加法

`$core.add`两数相加，返回两数的和。

### 语法

> $core.add(augend, addend)

#### 参数

- augend 非必填，加数
- addend 非必填，被加数

#### 返回值

返回两数的和，和可以使数值`Number`类型或者大整数`BigInt`类型。

### 例子

```javascript
$core.add(1, 2); // 3
$core.add(1, 2n); // 3 不推荐
$core.add(1n, 2n); // 3n
$core.add(0.1, 0.2); // 0.3
```

---

## 减法

`$core.sub`两数相减，返回两数的差。

### 语法

> $core.sub(minuend, subtrahend)

#### 参数

- minuend 非必填，被减数
- subtrahend 非必填，减数

#### 返回值

返回两数的差，差可以使数值`Number`类型或者大整数`BigInt`类型。

### 例子

```javascript
$core.sub(3, 2); // 1
$core.sub(3, 2n); // 1
$core.sub(3n, 2n); // 1n
$core.sub(0.3, 0.2); // 0.1
```

---

## 乘法

`$core.mul`两数相乘，返回两数的积。

### 语法

> $core.mul(multiplier, multiplicand)

#### 参数

- multiplier 非必填，乘数
- multiplicand 非必填，被乘数

#### 返回值

返回两数的积，积可以使数值`Number`类型或者大整数`BigInt`类型。

### 例子

```javascript
$core.mul(1, 2); // 2
$core.mul(1, 2n); // 2
$core.mul(1n, 2n); // 2n
$core.mul(0.1, 0.2); // 0.02
```

---

## 除法

`$core.div`两数相除，返回两数的商。

### 语法

> $core.div(dividend, divisor)

#### 参数

- dividend 非必填，被除数
- divisor 非必填，除数

#### 返回值

返回两数的商，商可以使数值`Number`类型或者大整数`BigInt`类型。

### 例子

```javascript
$core.div(1, 2); // 0.5
$core.div(1, 2n); // 0.5
$core.div(1n, 2n); // 0n
$core.div(0.1, 0.2); // 0.5
```

---

## 最小值

`$core.min`方法找到数组中最小元素的项，如果是空数组返回 undefine。

### 语法

> $core.min(array, iteratee)

#### 参数

- array 数组，默认获取数值中最小的元素。
- iteratee 非必填，数组中的元素按照 iteratee 函数规则获取最小的元素。

#### 返回值

返回数组中最小的元素，如果是空数组返回 undefined。

### 例子

#### 例一、

```javascript
$core.min([3, 1, 9, 5, 7]); // 1
```

#### 例二、

```javascript
$core.min([
  { name: 'a', age: 3 },
  { name: 'b', age: 1 },
  { name: 'c', age: 9 },
  { name: 'd', age: 5 },
  { name: 'e', age: 7 },
]); // { name: 'b', age: 1 }
```

## 最大值

`$core.max` 方法指找到数组中最大元素的项，如果是空数组返回 undefine。

### 语法

> $core.max(array, iteratee)

#### 参数

- array 数组，默认获取数值中最小的元素。
- iteratee 非必填，数组中的元素按照 iteratee 函数规则获取最小的元素。

#### 返回值

返回数组中最大的元素，如果是空数组返回 undefined。

### 例子

#### 例一、

```javascript
$core.max([3, 1, 9, 5, 7]); // 9
```

#### 例二、

```javascript
$core.max([
  { name: 'a', age: 3 },
  { name: 'b', age: 1 },
  { name: 'c', age: 9 },
  { name: 'd', age: 5 },
  { name: 'e', age: 7 },
]); // { name: 'c', age: 9 }
```

## 求和

### 语法

> $core.sum(array, iteratee)

#### 参数

- array 数组。
- iteratee 非必填，数组中的元素按照 iteratee 函数规则的返回值进行累加求和。

#### 返回值

返回数组中元素的和。

### 例子

#### 例一、

```javascript
$core.sum([3, 1, 9, 5, 7]); // 25
```

#### 例二、

```javascript
$core.sum(
  [
    { name: 'a', age: 3 },
    { name: 'b', age: 1 },
    { name: 'c', age: 9 },
    { name: 'd', age: 5 },
    { name: 'e', age: 7 },
  ],
  function (item) {
    return item.age * 10;
  }
); // 25
```

## 平均值

```javascript
$core.mean([3, 1, 9, 5, 7]); // 5
```

```javascript
$core.mean(
  [
    { name: 'a', age: 3 },
    { name: 'b', age: 1 },
    { name: 'c', age: 9 },
    { name: 'd', age: 5 },
    { name: 'e', age: 7 },
  ],
  function (item) {
    return item.age * 10;
  }
); // 5
```
