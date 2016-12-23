# 日期对象的使用:(当前时间是2016年12月23日  15:22:33)
* console.log(new Date());                返回值: Fri Dec 23 2016 11:10:59 GMT+0800 (CST)  
* console.log(new Date().getTime());      返回值:1482462777844  (返回从 1970 年 1 月 1 日至今的毫秒数。)  
* console.log(new Date().toUTCString());  返回值:Fri, 23 Dec 2016 03:15:12 GMT(将当日的日期（根据 UTC）转换为字符串。)   

* typeof new Date();                      返回值:object  
* typeof new Date().toUTCString();        返回值:"string"  

 表示月份的参数介于 0 到 11 之间。也就是说，如果希望把月设置为 8 月，则参数应该是 7。  
* console.log(new Date().setFullYear(2008,7,9));    返回值: 720774948007  (为日期对象设置了一个特定的日期 (2008 年 8 月 9 日))
* console.log(new Date().getFullYear());            返回值: 2016  
* console.log(new Date().getMonth());               返回值: 11 (返回的数值+1=当前的月份)  
* console.log(new Date().getDate());                返回值: 23 (返回的数值+1=当前的月份)  
* console.log(new Date().getDay());                 返回值: 5 (星期一:1;星期二:2;星期三:3;星期四:4;星期五:5;星期六:6;星期日:0;)  
* console.log(new Date().getHours());               返回值: 15 (返回当前的小时数24小时制)  
* console.log(new Date().getMinutes());             返回值: 22 (返回当前的分钟数)  
* console.log(new Date().getSeconds());             返回值: 33 (返回当前的秒数)  

# 日期对象的格式转换
UTC时间与毫秒数之间的转换:  

UTC时间==>毫秒数:  用 UTC时间.getTime();
UTC时间: new Date();  
毫秒数:  new Date().getTime();  

毫秒数==>UTC时间:  用new Date(毫秒数);  
毫秒数:  new Date().getTime();  
UTC时间: new Date(new Date().getTime());  

# 日期大小的比较(UTC时间和毫秒数都是可以比较大小的)  
var myDate=new Date();
myDate.setFullYear(2008,7,9); // 为日期对象设置了一个特定的日期 (2008 年 8 月 9 日)
var today = new Date();
console.log(today>myDate);

# 最近4年(包含当年)setYear()    返回值是毫秒数
* const now=new Date();  
new Date(now.setYear(now.getFullYear()-3));    返回值: Mon Dec 23 2013 17:09:00 GMT+0800 (CST)  

# 最近4个月(包含当月)setMonth()  返回值是毫秒数
* const now=new Date();  
new Date(now.setMonth(now.getMonth()-3));      返回值: Fri Sep 23 2016 17:10:04 GMT+0800 (CST)  

# 最近4天(包含当天)setDate()    返回值是毫秒数
* 如果增加天数会改变月份或者年份，那么日期对象会自动完成这种转换。  (当前时间2016.12.23.16:55:51)    
var myDate=new Date();    
new Date(myDate.setDate(myDate.getDate()-3));  返回值: Tue Dec 20 2016 16:55:51 GMT+0800 (CST)  
{myDate.setDate(myDate.getDate()-5)是毫秒数}   

# 最近4小时(包含当下的小时)setHours()    返回值是毫秒数
* const now=new Date();  
new Date(now.setHours(now.getHours()-3));    返回值: Mon Dec 23 2013 17:09:00 GMT+0800 (CST)  

# 最近4分钟(包含当下的分钟)setMinutes()    返回值是毫秒数
* const now=new Date();  
new Date(now.setMinutes(now.getMinutes()-3));    返回值: Mon Dec 23 2013 17:09:00 GMT+0800 (CST)  

# 最近4分钟(包含当下的秒数)setSeconds()    返回值是毫秒数
* const now=new Date();  
new Date(now.setSeconds(now.getSeconds()-3));    返回值: Mon Dec 23 2013 17:09:00 GMT+0800 (CST)  
