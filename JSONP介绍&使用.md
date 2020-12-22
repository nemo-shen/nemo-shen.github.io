# JSONP介绍&使用

>1. jsonp是json的一种变体，主要包含**回调**和**数据**两部分
>2. 通过jsonp我们可以在别的域名获取数据
>3. jsonp调用通过动态创建script元素并为src属性执行跨域URL实现
>4. jsonp是有效JavaScript代码，所以jsonp响应在完成加载后会被立即执行

## 简单使用

当前网页地址：www.a.com

jsonp请求地址：http://www.api.com/json?callback=handleResponse

jsonp返回数据：handleResponse({"status": 100, "errMsg": "ok", "data": [1,2,3]})

```js
function handleResponse(response) {
  console.log('response: ', response)
}

let jsonpURL = "http://api.com/json?callback=handleResponse"
// response = handleResponse({"status": 100, "errMsg": "ok", "data": [1,2,3]})
let script = document.createElement('script')
script.src = jsonpURL
document.body.insertBefore(script, document.body.firstChild)
// script加载完成后会立即执行handleResponse(response)
```

## 优势

1. 利用jsonp可以避开浏览器同源策略，进行跨域访问
2. jsonp由于它的特点，我们可以在callback里面处理响应数据
3. 简单易用

## 缺点

1. jsonp由于在响应完成后会立即执行，所以一定要确保jsonp拉取域名的数据可信度
2. 由于script的onerror事件还没有被浏览器实现，所以不好确定是否加载失败