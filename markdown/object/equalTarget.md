# $core.equalTarget

`$core.equalTarget` 判断对象键值对是否一样。

## 语法

> $core.equalTarget(targetA, targetB, isStructure = false);

### 参数

- targetA 待比较对象一
- targetB 待比较对象二
- isStructure 如果为 true，仅比较结构

### 返回值

返回对象

## 例子

### 例一、

```javascript
$core.equalTarget({}, {}); // true
$core.equalTarget([], []); // true
```

### 例二、

```javascript
$core.equalTarget({ name: "qianduanka" }, { name: "qianduanka" }); // true
$core.equalTarget([1, 3, 5, 7, 9], [1, 3, 5, 7, 9]); // true

$core.equalTarget(
  { name: "qianduanka", value: 3 / 0 },
  { name: "qianduanka", value: 5 / 0 }
); // true
$core.equalTarget([1, 3 / 0, 5, 7, 9], [1, 33 / 0, 5, 7, 9]); // true
```

### 例三、

```javascript
console.log($core.equalTarget("qianduanka", "qianduanka")); // true
console.log($core.equalTarget(3 / 0, 5 / 0)); // true
```

### 例四、

```javascript
$core.equalTarget({ name: "qianduanka" }, { name: "qdk" }, true); // true
```
