

# 综述



1. js是基于==事件模型==的程序语言，页面加载、用户点击、移动光标等都会产生事件。当事件产生时，js就可以调用某个函数来针对这个事件做出响应。









# 1.基本概念

## 1.1重要语句

1. `document.getElementById()`

   这是js的id选择器！！！

   ```html
   <script type="text/javascript">
       //定义加密函数
       function encrypt() {
           //获取输入框的值
           var str = document.getElementById("txt-input").value;
           //将输入框的值加密，并赋给输出框
           document.getElementById("txt-ouput").value = escape(str);
       }
   </script>
   ```

   

   

# 3.函数

## 3.1概述

1. js是基于==事件模型==的程序语言，页面加载、用户点击、移动光标等都会产生事件。当事件产生时，js就可以调用某个函数来针对这个事件做出响应。

2. 使用`function`关键字定义函数

3. js和其他编程语言的函数的最大区别在于它的调用方式很多，很灵活。

   + 简单调用
   + 在表达式中调用
   + 在事件响应中调用
   + 通过链接调用

4. js的特殊函数有三种

   + 嵌套函数

     就是在一个函数的内部定义另外一个函数。不过在内部定义的函数只能在内部调用。

   + 递归函数

   + 内置函数(即js内部已经实现好的函数)





## 3.2内置函数

### 3.2.1eval()

1. 作用

   `eval()`可以把一个字符串当做一个js表达式一样去执行它。

2. 语法

   `eval(string)`



### 3.2.2isFinite()

1. 作用

   用来确定某一个数是否是一个有限数值

2. 语法

   `isFinite(number)`



### 3.2.3isNaN()

1. 作用

   判断是不是NaN类型

2. 注意

   如果参数是==字符串类型的数字==，就会自动转换为数字型



### 3.2.4parseInt()和parseFloat()

1. 作用

   将首位为数字的string转化为数字。如果字符串不是以数字开头，则返回NaN。

2. PS：

   如果一个字符串跟一个数字相加，js会将数字转化为字符串，然后在进行==拼接==。



### 3.2.5escape()和unescape()

1. 作用

   `escape()`函数主要作用就是对字符串进行编码，以便它们能在所有计算机上可读。

2. 语法

   `escape(charString)`





# 4.内置对象

## 4.1字符串对象String

1. 长度属性

   `str.length`

2. match()

   + 用来检索一个字符串是否存在，存在就返回要检索的字符串，如果不存在返回null

   + 语法

     ```javascript
     stringObject.math(字符串) //匹配字符串
     stringObject.math(正则表达式) //匹配正则表达式
     ```

3. search()

   + 用于检索字符串中指定的字符串，或检索与正则表达式相匹配的子串
   + 返回的是子串的起始位置，如果没有找到则返回-1

4. indexOf()

   + 返回某个指定的字符串在字符串中==首次出现的位置==，没有找到则返回-1

   + 语法

     `stringObject.indexOf(字符串)`

5. replace()

   + 用一些字符替换另一些字符，或者替换一个与正则表达式相匹配的子串

   + 语法

     ```javascript
     stringObject.replace(原字符串，替换字符串)
     stringObject.replace(正则表达式，替换字符)
     ```

6. charAt()

   + 含义

     ```javascript
     stringObject.charAt(0) 相当于 C++中的stringObject[0]
     ```

7. 英文大小写转换

   ```javascript
   string.toLowerCase() //转小写
   string.toUpperCase() //转大写
   ```

8. 字符串拼接

   ```javascript
   //方法一
   str1.concat(str2, str3, str4....)
   
   //方法二
   str = str1 + str2 + str3 + ...
   ```

9. 比较字符串

   + 在js中，可以使用`localeCompare()`方法用本地特定顺序来比较这两个字符串

   + 语法

     ```javascript
     str1.localeCompare(str2)
     
     //返回值与strcmp相同
     ```

10. 分割字符串

    + 语法

      `string.split(分割符)`

      ==分割符可以是一个字符、多个字符或一个正则表达式，分割符不作为返回数组元素的一部分==

    + ```javascript
      var str = "I love javascript!"
      var arr = new Array();
      arr = str.split(" ");
      document.write(arr);
      //输出的是I,love,javascript!
      ```

11. 提取字符串

    + 使用`substring()来提取字符串中的某一部分字符串`

    + 语法

      ```javascript
      stringObject.substring(start, end)
      ```

      

## 4.2日期对象Date

1. 创建Date对象

   ```javascript
   //方法一，用于获取当前系统的时间
   var date = new Date();
   
   //方法二，自己设置的时间
   var date = new Date(日期字符串);
   //日期字符串可以是以下几种形式
   //"2020-9-29"     "September 29, 2020"    "2020/9/29"
   ```

2. 日期对象的方法

   日期对象的方法主要分为三大组：`setXxx(用于设置)、getXxx(用于获取)、toXxx(将日期转换为指定格式)`

   ![img](https://wx3.sinaimg.cn/mw690/005LasY6ly1gjc5t7tthnj30u00xb7fe.jpg)

   



## 4.3数组对象Array

1. 创建数组对象

   ```javascript
   //新建一个长度为0的数组
   var arr = new Array();
   
   //新建一个长度为3的数组
   var arr = new Array(3)；
   
   //新建指定长度的数组并赋值
   var arr = new Array(1, 2, 3, 4);
   ```

2. Array对象的属性

   ```javascript
   //常用，获取数组长度
   arr.length
   
   arr.constructor
   
   arr.prototype
   ```

3. Array对象的方法

   ![img](https://wx3.sinaimg.cn/mw690/005LasY6ly1gjc65zlfjcj311a0u0dlf.jpg)

4. PS：

   ==js中的一个Array对象中是可以存储不同类型的元素的，但是实际开发中很少用到！==

   



## 4.4数值对象Math和Number

1. js中，数值对象共有2中

   + Number
   + Math

   然而，很少使用Number对象，所以目前只学习Math对象

2. 在js中，Math对象时==无需==使用new关键词创建的，这一点和Date对象、Array对象不同！！因此我们可以直接调用Math对象的属性和方法。

3. Math对象的属性

   + Math对象的属性往往都是数学中常用的”常量“，如下

   ![img](https://wx4.sinaimg.cn/mw690/005LasY6ly1gjc6usndd4j313s0lodkw.jpg)

   + 用法

     ```javascript
     var pi = Math.PI;
     ```

     

4. Math对象的方法

   Math对象的方法是数学中常用的函数，如下

   ![img](https://wx2.sinaimg.cn/mw690/005LasY6ly1gjc6x6bv6bj30u00v5n71.jpg)

   



# 5.内置的重要的对象

## 5.1window对象

1. 简而言之，window对象就是用来操作”==浏览器窗口==“的一个对象。

   + 一个浏览器窗口就是一个window对象。
   + window对象是js中最核心的对象，document、history对象等都是window对象的子对象。

2. window对象属性

   入门阶段一个都用不着。

3. window对象方法

   ![img](https://wx4.sinaimg.cn/mw690/005LasY6ly1gjc8gshekij30y20jmgp0.jpg)

   由于内容太多。。不想记了，so贴个url。。。

   http://www.lvyestudy.com/les_js/js_list.aspx

4. ==***<u>对话框方法</u>***==

   + 在js中，对话框共有3种
     + alert();
     + confirm();
     + prompt();
   + 这三种方法都属于window对象，其实alert()方法完整写法是”window.alert()“，但是由于window对象时全局对象，我们简写成"alert()"即可， confirm()和promot()也是同样的道理。
   + 这三种对话框特点如下：
     + alert()仅有提示文字，没有返回值
     + confirm()具有提示文字，返回”bool“值
     + prompt()具有提示文字，返回”字符串“



## 5.2document对象

1. 顾名思义，document对象操作的都是==html文档==。

2. document对象时window对象的子对象。

3. 对象属性

   ![img](https://wx4.sinaimg.cn/mw690/005LasY6ly1gjcco8srljj313w0rgafi.jpg)

4. 对象方法

   ![img](https://wx4.sinaimg.cn/mw690/005LasY6ly1gjccoo2aadj31600d441q.jpg)

   