# Array.prototype.slice.call()使用解释

> Array.prototype.slice(?start, ?end) 方法可以截取数组

## 基础使用方法

```js
let arr = [1,2,3]
arr.slice() // [1,2,3]
arr.slice(0, 1) // [1]
arr.slice(1, 2) // [2,3]
```

## Array.prototype.slice.call(arr, ?start, ?end)

> 此用法能将**带有length属性的对象**转换成数组

### 用法

```js
let obj = {0: 'foo', 1: 'bar', 2: 'baz', 3: 'qux', length: 4}
Array.prototype.slice.call(obj) // ['foo', 'bar', 'baz', 'qux']
Array.prototype.slice.call(obj, 0) // ['foo', 'bar', 'baz', 'qux']
Array.prototype.slice.call(obj, 1) // ['bar', 'baz', 'qux']
Array.prototype.slice.call(obj, 1, 3) // ['bar', 'baz']

// 删除length属性后无法正确返回数组
delete obj.length
Array.prototype.slice.call(obj) // []
```



## 参考资料：

[Array.prototype.slice.call()方法详解](https://www.jianshu.com/p/c5df0156b229)

