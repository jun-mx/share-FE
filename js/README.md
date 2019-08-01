### 一.JavaScript的简史
   1. 1995年的时候   由网景公司(Netscape)开发的，当时的名字叫livescript    为了推广自己的livescript，搭了java顺风车，改名为javascript。
与此同时，微软也在自己的浏览器里推出了自己的脚本语言jsscript。
Netscape

2. 1997年时候，  由ECMA(欧洲计算机制造商协会)出面，推出了一套javascript的规范，Ecmascript ,规范提出js由三部分组成 
   + ECMAScript         基础语法
   + DOM   	文档对象模型
   + BOM 		浏览器对象模型 

3. 2003之前，网页界面上的弹窗广告几乎都是由js做的，被人称做牛皮癣。
4. 2004年的时候，JS的命运发生改变   ajax(谷歌公司)出现。
5. 2007的时候  苹果公司推出的手机，可以用来上网，移动端页面开始流行。
6. 2010的时候  H5的出现    canvas  又推高了js的地位
7. 2011年的时候， node.js   将js这种语言伸向后服务器端

**注1：**
后来，微软通过IE击败了Netscape后一统桌面，结果几年时间，浏览器毫无进步。（2001年推出的古老的IE 6到今天仍然有人在使用！）
没有竞争就没有发展。微软认为IE6浏览器已经非常完善，几乎没有可改进之处，然后解散了IE6开发团队！而Google却认为支持现代Web应用的新一代浏览器才刚刚起步，尤其是浏览器负责运行JavaScript的引擎性能还可提升10倍。
先是Mozilla借助已壮烈牺牲的Netscape遗产在2002年推出了Firefox浏览器，紧接着Apple于2003年在开源的KHTML浏览器的基础上推出了WebKit内核的Safari浏览器，不过仅限于Mac平台。
随后，Google也开始创建自家的浏览器。他们也看中了WebKit内核，于是基于WebKit内核推出了Chrome浏览器。

**注2：**
有个叫Ryan Dahl的歪果仁，2009年，推出了基于JavaScript语言和V8引擎的开源Web服务器项目，命名为Node.js。
Node.js是一个javascript运行环境。它让javascript可以开发后端程序，实现几乎其他后端语言实现的所有功能，可以与PHP、Java、Python、.NET、Ruby等后端语言平起平坐。

### 二.JavaScript能做什么
* 网页上特效：轮播图、tab选项卡...
* 表单数据验证
* 可以和服务器交互，异步交互
* 做服务端（nodejs）
* 游戏开发

### 三.JavaScript的特点

* 简单易用：
编写很简单的，只需要记事本就能编写
* 执行的环境很简单：
只需要浏览器就可以执行

* 解释执行：
当需要执行的时候才去检查代码是否符合语法规范，边解释边执行。
* 单线程
 JavaScript引擎是单线程运行的,浏览器无论在什么时候都只且只有一个线程(一个队列)在运行JavaScript程序。（记住这句话）
* 基于对象：
对象主要是指js内置的对象，内部有很多方法和对象，可以方便的调用，简单代码实现复杂逻辑。

### 四.变量
* **什么是变量**
   * 变量就是容器，容器里装着数据（简单理解）
   * 变量真正来说存储的是指向存储数据的位置

* **变量命名规范**
   * 取值的范围：字母、数字、下划线、$
   * 不能使用数字开头
   * 不推荐用中文命名，推荐使用有意义的单词命名
   * 严格区分大小写
   * 不能使用保留字和关键字
   * 一般采用驼峰写法，第一个单词首字母小写，第二个单词搜字母大写：userName。
> **关键字**： 有特殊功用的单词就叫做关键字;
     **保留字**： 未来可能做为关键字的存在

![关键字](https://upload-images.jianshu.io/upload_images/7525071-cc815cfa1e7de711.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/940)

![保留字](https://upload-images.jianshu.io/upload_images/7525071-a31e9aaceeb3b9d2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 五.数据类型
* **介绍**：js中有六种数据类型，包括五种基本数据类型（Number,String,Boolean,Undefined,Null）,和一种复杂数据类型（Object）。在基本类型中又有两种特殊类型：Undefined、Null。
* **typeof 运算符**
可以判断以上六种数据类型
typeof (数据)
* **Number-数字类型**
   1.所有的数字，整数、小数、正数、负数。
   2.NAN: 不是数字的数字：Number("非数字类型数据")

* **String-字符串类型**
用""或''包起来的数据："2345"、"我是字符串"

* **Boolean-布尔类型**
该类型只有两个值，true和false；
一般用在判断语句里，表示条件是否成立

````
if(true){console.log('他是对的')}
````

* **Undefined**
未定义的变量
* **Null**
尚未存在的对象（空对象）

* **Object-对象**

**描述：**
js中对象是一组属性与方法的集合。这里就要说到引用类型了，引用类型是一种数据结构，用于将数据和功能组织在一起。引用类型有时候也被称为对象定义，因为它们描述的是一类对象所具有的属性和方法。
示例：Date、Array

`var time = new Date()`

### 六.数据类型转换
* **数字转换为字符串**
**1.	数字 + ""** （隐式转换：js在执行代码时自己将数据类型进行转换）

`3+"2"`


**2.	String(数字)** （显示转换：我们手动转换）

`String(123)`


**3.	数字.toString()**

`var aa = 22; aa.toString();`


* **将字符串转换为数字**

**1. 	+ "数字"** （隐式转换）

`+ "12"`


**2.	Number("数字")**（显示转换）

`Number("12")`


**3.	parseInt()、parseFloat()**

`parseInt("123.12")`转换为整数
`parseFloat("123.12")`转换为小数


* **转换为布尔类型**

**1	!!数据**	(隐式转换)	

`!!23`

**2	Boolean(数据)**	(显示转换)	

`Boolean(12)`

* **注1：**下面6种值转化为布尔值时为false，其他转化都为true
   1. undefined（未定义，找不到值时出现）
   2. null（代表空值）
   3. false（布尔值的false，字符串"false"布尔值为true）
   4. 0（数字0，字符串"0"布尔值为true）
   5. NaN（无法计算结果时出现，表示"非数值"；但是typeof NaN==="number"）
   6. ""（双引号）或''（单引号） （空字符串，中间有空格时也是true）

### 七.运算符

* **算术运算符**

    **\+ 加号运算**
1. 数字+数字的时候  得到两个数字的和。

`2 + 3 = 5`


2. 字符串 + 字符串  得到的结果是字符串相互拼接

`"2" + "3" = "23"`


3. 数字 + 字符串 	得到的结果是字符串

`2 + "3" = "23"  //相当于把数字转化成字符串，然后进行拼接`

   **\- 减号运算**
    
1. 数字 - 数字   得到两个数字的差

`5 - 3 = 2`

2. 字符串 - 字符串（隐式转换为数字类型）

`"5" - "2" = 3  //以数字为内容的字符串相减得到数字(隐式转换)` 
`"32" - "减" = NaN    //不以数字为内容的字符串相减 得到NaN` 


   **\*	乘号运算**
1. 数字 * 数字    得到两个数字的乘积

`2 * 3 = 6`

2. 字符串 * 字符串 (隐式转换为数字类型）

`"2" * "3" = 6`
` "2" * "乘" = NaN`


   **/      除号运算**
1. 数字 / 数字    得到两个数字的相除的商

`6 / 2 = 3`


2. 字符串 / 字符串（隐式转换为数字类型）

`"6" / "2" = 3`
`"6" / "除" = NaN`


   **注1：** 除了+，其余的三个运算符都会讲字符串转化为数字类型

* **判断运算符**

   > 
   < 
   >=  
   <=  
   == 
   !=
   !== 
   ===

* **=== 和==的区别**

== 用于比较、判断两者相等，如果两个不同数据类型的值比较时先自动换数据类型;
===  用于（严格）比较、判断两者（严格）相等，不会进行自动转换，要求进行比较的操作数必须类型一致，不一致时返回flase。

**注1：**  ==和!=转换的基本准则如下：
  1. 如果有一个操作数是布尔值，则在比较之前先将其转换为数值，false转换为0，true转换为1。
 
 `true == 1  //ture`
   `false == 0  //true` 

 2. 如果一个操作数是字符串，另一个操作数是数值，在比较相等性之前先将字符串转为数值。

`"12" == 12 //true`

 3. null和undefined是相等的。
 
 `null == undefined //true`
 
 4. NaN不等于NaN。
  
  `NaN == NaN //false`


  **注2：** 全等的严格模式

`"12" === 12 //false`

### 八、定时器

* setInterval 循环定时器/ clearInterval清除定时器

````
var timer = setInterval(function(){
  console.log("setInterval");
},1000)
clearInterval(timer);
````

* setTimeout 延时定时器/ clearTimeout清除定时器

````
var timer = setTimeout(function(){
  console.log("setInterval");
},1000)
clearTimeout(timer);
````

**注1：** 两种定时器的应用场景
setInterval是间隔设定时间循环执行，用在需要轮询执行的逻辑中；
setTimeout是在延时设定时间后只执行一次，用在一个需要在当前时间延时指定时间执行的逻辑

### 九、循环语句

* **while**

````
var a = 1;
 while(a<=100){
       console.log(a);
       a++; //如果a++忘记写，则会陷入死循环
   }
````

* **do……while**

````
var a = 0;
do{
    console.log(a)
    a++
}while(a <= 10)
````

* **for**

````
var c = 0;
for(var i = 0; i < 10; i++){
    console.log(c);
    c++
}
````

**注1：** while循环很危险
只要指定条件为 true，循环就可以一直执行代码。如果您忘记增加条件中所用变量的值，该循环永远不会结束。该可能导致浏览器崩溃。
[http://www.w3school.com.cn/js/js_loop_while.asp](http://www.w3school.com.cn/js/js_loop_while.asp)

**注2：** 数组和对象自己的循环逻辑
  1. 数组：foreach、map
  2. 对象：for-in

````
//foreach
var arr = [1,2,3,4]
arr.forEach(function(value,i){
　　console.log('forEach遍历:'+ i +'--'+ value);
})
//map
arr.map(function(value,index){
   console.log('forEach遍历:'+ index +'--'+ value);
});
//for-in
//对象里的值是以键值对的形式存储
var obj = {a:1, b: 2}
for (var key in obj){
    console.log(obj[key]);
    console.log(key);
}


````


### 十、异步和同步

* **什么是同步**
后一个任务等待前一个任务结束，然后再执行，程序的执行顺序与任务的排列顺序是一致的、同步的，按照队列一步步执行。

* **什么是异步**
简单说就是一个任务分成两段，先执行第一段，然后转而执行其他任务，等做好了准备，再回过头执行第二段。

* **为什么要异步**
因为js是单线程的，但是有很多情况的执行步骤（如ajax请求远程数据）是非常耗时的，如果一直单线程的堵塞下去会导致程序的等待时间过长页面失去响应，影响用户体验了。
如何去解决这个问题呢，我们可以这么想。耗时的我们都扔给异步去做，做好了再通知下我们做完了，我们拿到数据继续往下走。

* **异步常见的例子**
   1. ajax请求   
   2. setTimeout

注1：ajax异步示例

````
var aa = 4;
$.getJSON("https://www.easy-mock.com/mock/5b98722937496f558cf63073/example/starList").then(function(res){
    console.log("请求成功");
})

console.log("请求后");
console.log("请求后1");
for(var i=0; i<500; i++){
    aa++
}
console.log(aa);
````

注2：setTimeout异步示例
 ```` 
var aa = 1;
setTimeout(function() {
    console.log("setTimeout");
}, 0);

console.log("请求后");
for(var i=0; i<500; i++){
    aa++
}

console.log(aa);
````

* **事件循环**

**介绍：** JS 会创建一个类似于 while (true) 的循环，每执行一次循环体的过程称之为 Tick。每次 Tick 的过程就是查看是否有待处理事件，如果有则取出相关事件放入执行栈中由主线程执行。这些待处理的事件会存储在一个**任务队列**中，也就是每次 Tick 会查看任务队列中是否有需要执行的任务。


* **任务队列**

**介绍：** js按照主线程的队列异步操作会将相关回调添加到任务队列中。而不同的异步操作添加到任务队列的时机也不同，如 onclick, setTimeout, ajax 处理的方式都不同，这些异步操作是由浏览器内核的 webcore 来执行的，webcore 包含3种 webAPI，分别是 DOM Binding、network、timer模块。
  1. onclick 由浏览器内核的 DOM Binding 模块来处理，当事件触发的时候，回调函数会立即添加到任务队列中。
  2. setTimeout 会由浏览器内核的 timer 模块来进行延时处理，当时间到达的时候，才会将回调函数添加到任务队列中。
  3. ajax 则会由浏览器内核的 network 模块来处理，在网络请求完成返回之后，才将回调添加到任务队列中。

* **主线程**
JS 只有一个线程，称之为主线程。而**事件循环**是主线程中执行栈里的代码执行完毕之后，才开始执行的。所以，主线程中要执行的代码时间过长，会阻塞事件循环的执行，也就会阻塞异步操作的执行。只有当主线程中执行栈为空的时候（即同步代码执行完后），才会进行事件循环来观察要执行的事件回调，当事件循环检测到任务队列中有事件就取出相关回调放入执行栈中由主线程执行。

### 十一、Ajax / json

* **Ajax的含义和意义**

**含义：** Asynchronous Javascript And XML（异步JavaScript和XML）,他并不是凭空出现的新技术,而是对于现有技术的结合，核心是js的异步对象：XMLHttpRequest。
http://www.w3school.com.cn/ajax/ajax_xmlhttprequest_create.asp

**意义：** 在不刷新页面的情况下，去获取服务器信息。
当我们访问一个普通的网站时,当浏览器加载完:HTML,CSS,JS以后网站的内容就固定了.如果网站内容发生更改必须刷新页面才能够看到更新的内容。有了ajax，在浏览器中,我们也能够不刷新页面,通过ajax的方式去获取一些新的内容,类似网页有微博,朋友圈,邮箱等，还有下拉刷新。

* **原生ajax的写法----五步使用法**
  1. 建立XMLHTTPRequest对象
  2. 注册回调函数
当服务器回应我们了,我们想要执行什么逻辑
  3. 使用open方法设置和服务器端交互的基本信息
设置提交的网址,数据,post提交的一些额外内容
  4. 设置发送的数据，开始和服务器端交互
发送数据
  5. 更新界面
在注册的回调函数中,获取返回的数据,更新界面

````
    // 创建XMLHttpRequest 对象
    var xml = new XMLHttpRequest();

    // 设置跟服务端交互的信息
    xml.open('get','https://www.easy-mock.com/mock/5b98722937496f558cf63073/example/starList');
    xml.send(null);    // get请求这里写null即可

    // 接收服务器反馈
    xml.onreadystatechange = function () {
        // 这步为判断服务器是否正确响应
        if (xml.readyState == 4 && xml.status == 200) {
            // 打印响应内容
            console.log(xml.responseText);
        } 
    };
````

**注1：** onreadystatechange 中readyState 的状态值
0: 请求未初始化
1: 服务器连接已建立
2: 请求已接收
3: 请求处理中
4: 请求已完成，且响应已就绪
 
**注2：** JQ中ajax的调用
http://www.w3school.com.cn/jquery/jquery_ref_ajax.asp


### 十二.js书写位置

* **script标签里**

````
<script type="text/javascript">
        // 在这里写js代码
</script>
````

注：必须写在相关元素的后边

* **引入js文件**

````
<script src="xx/index.js"></script>
````


* **引入js的位置**
一般在模板最后(dom渲染结束后)，引入业务相关js.
一行一行的执行，调用也是按照先后顺序，一处报错，后边的代码不再执行。按照页面渲染的顺序去调用。
注：当前项目的交互代码在整个页面渲染完成后引入


### 十一.调试

* **调试方法**

`alert()`
`console.log()`
`return`

以上方法通常配合使用，alert和console可以弹出和打印相关信息，return可以中断js的执行队列，不再往下进行。
如果你在调试的时候不想请求某个接口或者不想执行某个交互(节点隐藏)，可以在前边加上return。

* **常见报错信息**

**undefined**
已经声明过，但未赋值的变量，报错----存在没有内容

**not defined**
没有声明过的变量，报错 ---- 不存在

**xxx is not a function**
该对象没有这个方法，大部分情况是这个对象是没有赋值成功，找不到对应类型的方法
