# 日期对象的使用:  
* console.log(new Date());                返回值: Fri Dec 23 2016 11:10:59 GMT+0800 (CST)  
* console.log(new Date().getTime());      返回值:1482462777844  (返回从 1970 年 1 月 1 日至今的毫秒数。)  
* console.log(new Date().toUTCString());  返回值:Fri, 23 Dec 2016 03:15:12 GMT(将当日的日期（根据 UTC）转换为字符串。)  

* typeof new Date();                      返回值:object  
* typeof new Date().toUTCString();        返回值:"string"  

* console.log(new Date().getFullYear());  返回值: 2016
* console.log(new Date().getMonth());     返回值: 11  
