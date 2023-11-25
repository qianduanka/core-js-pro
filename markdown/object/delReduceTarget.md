# $core.delReduceTarget

`$core.delReduceTarget` 方法用于按照描述删除字段精简化对象数据结构。

## 语法

> $core.delReduceTarget(target, descTarget);

### 参数

- target 待精简化对象
- descTarget 精简化描述结构

### 返回值

返回精简化后的新对象。

## 例子

### 例一、

```javascript
$core.delReduceTarget(
  { name: "qianduanka", age: 25 },
  {
    age: $core.DEL,
  }
);

// { "name": "qianduanka" }
```
