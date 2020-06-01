# 这个仓库的主要是关于组件的制作
## site-topbar是关于网页头部的制作  
## time-dates时间格式转换与日期详细描述  
```jsx
js实现滚动到网页顶部：
- []document.scrollingElement.scrollTop = 0;
    参考文档：https://developer.mozilla.org/zh-CN/docs/Web/API/Document/scrollingElement
- [] window.scrollTo()
    参考文档： https://m.runoob.com/jsref/met-win-scrollto.html

```

```jsx
 js toLocaleString()方法：
 - [] 把数组转换为字符串;[1,2,3].toLocaleString() 输出 '1,2,3'
 - [] 如果数字使用，则会把数字格式化为按照三位一逗号的形式，最大保留三位小数；
      参考链接：https://www.w3school.com.cn/jsref/jsref_toLocaleString_array.asp
```

```jsx
xss攻击：跨站脚本攻击， cross site scripting
```

```jsx
  React中使用富文本；dangerousLySetInnerHTML

  <div dangerouslySetInnerHTML={{__html: "<div>1233</div>"}}/>

 - [] 参考文档：https://blog.csdn.net/exploringfly/article/details/80582859
```

```jsx
   let num = 123.205;
   num.toFixed(2) => "123.20";
   
   num = 123.235;
   num.toFixed(2) => "123.23";

   num = 123.225;
   num.toFixed(2) => "123.22";

   num = 123.005;
   num.toFixed(2) => "123.00";
```

```jsx
   let num;
   isNaN(num) => true  (Number(num) => NaN)
   
   num = "123abc";
   isNaN(num) => true  (Number(num) => NaN)

   num = "";
   isNaN(num) => false  (Number(num) => 0)

   num = "null";
   isNaN(num) => false  (Number(num) => 0)
 
   num = "123";
   isNaN(num) => false  (Number(num) => 123)
```

```jsx
 注意js中 / 操作符如果两侧的数字是整数，也会当作浮点数运算，不会整除，会保留小数
 const num = 5 / 2 // 2.5;
正确取整需要借助于parseInt();

向上取整一般用于分页计算
const totalPage=Math.ceil(totalRecord / pageSize)

```
