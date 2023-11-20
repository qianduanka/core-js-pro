# $core.sample

`$core.sample`方法用于随机获取数组中的元素。

## 语法

> $core.sample(collection = [])

### 参数

- collection 待打乱的集合。

### 返回值

返回打乱后的数组。

## 例子

### 例一、

```javascript
$core.shuffle(); // []
$core.shuffle([]); // []
$core.shuffle([1, 3, 5, 7, 9]); // [7, 1, 3, 5, 9] 参考：仅表示当次运行的返回值。
$core.shuffle(["a", "b", "c", "d", "e"]); // ["d","c","e","a","b"] 参考：仅表示当次运行的返回值。
```

### 例二、

```javascript
$core.shuffle("abcdef"); // ["c","b","e","d","a","f"] 参考：仅表示当次运行的返回值。
```

### 例三、

```javascript
$core.shuffle({ a: "aaa", b: "bbb", c: "ccc", d: "ddd", e: "eee", f: "fff" }); //["bbb","aaa","fff","ccc","ddd","eee"] 参考：仅表示当次运行的返回值。
```

### 例四、

```javascript
$core.shuffle(new Set(["a", "b", "c", "d", "e"])); // ["e","d","c","b", "a"] 参考：仅表示当次运行的返回值。
```

### 例五、

```javascript
$core.shuffle(
  new Map([
    ["a", "aaa"],
    ["b", "bbb"],
    ["c", "ccc"],
    ["d", "ddd"],
    ["e", "eee"],
  ])
); // ["bbb","eee","aaa","ccc","ddd"] 参考：仅表示当次运行的返回值。
```
