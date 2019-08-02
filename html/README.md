### 三驾马车
HTML			从语义的角度描述页面的结构（骨架）
CSS				从审美的角度美化页面（衣服）
JavaScript		从行为和交互的角度提升用户体验（动作）



### 一.什么是html

* **介绍：** Hypertext Markup Language（超文本标记语言）。超文本就是指页面内可以包含图片、链接，甚至音乐、程序等非文字元素。
HTML不是编程语言，不同于C语言、java或C#等编程语言，而是一种标记语言(markup language)，标记语言是由一套标记标签（markup tag）如<html></html>、<head></head>、<title></title>、<body></body>等组成。HTML就使用这些标记标签来描述网页。
html文件就是后缀名为html的文本, 可以在专业编辑器编辑，也可以在文本文档(如word)编辑后修改后缀名，如index.html。

   **注1：** 文档
   
  W3CSchool ：http://www.w3school.com.cn/

  菜鸟教程：https://www.runoob.com/html/html-tutorial.html 

   **注2：** 万维网/w3c
   
  万维网：通过超链接把众多超文本(html)连接起来可以相互访问的网络。

  W3C：万维网联盟，又称W3C理事会。最重要的工作是发展 Web 规范，1994年10月由万维网的发明者建立。

  https://baike.baidu.com/item/www/109924?fr=aladdin
  
* **结构** （h5）

  ````
  <!DOCTYPE html>				文档声明标记
  <html>						文档的开头和结尾
        <head>					放一些辅助显示的标签
           <title></title>			网页标题
        </head>			
         <body></body>			放我们能看见的标签
  </html>
  ````

### 二.html发展

* **简述：**
语言作为网络语言标准规范，在计算机的发展史中有着不可或缺的地位。在HTML上的成就也决定着一个时代的发展。

* **发展史：**
   + **HTML1.0：**实际上应该没有HTML1,所谓的HTML1是1993年IETF(互联网工作任务组)团队的一个工作草案，并不是成型的标准。
   
   + **HTML2.0：**1995年11月作为RFC1866发布，于2000年6月RFC2854发布之后宣布过时。
    http://www.rfc-editor.org/rfc/rfc1866.txt.
   
   + **HTML3.2：**1996年W3C撰写新规范，并于1997年1月推出HTML3.2。

   + **HML4.0与HTML4.0.1：**
   
      在1997年和1999年，作为升级版本的4.0和4.01也相继成为W3C的推荐标准。
  
      在2000年基于HTML4.01的ISO HTML成为了国际标准化组织和国际电工委员会的标准。于是被沿用至今，这期间虽然有点小的改动但大方向上终归没有什么变化。
  
      从1993-2000之间短短的7年时间，HTML语言有着很大的发展，基于诸多人的努力，终于产生了我们现在用的HTML语言。

   + **XHTML1.0：**
  
      2000年1月26日发布，是W3C的推荐标准，后于2002年8月1日重新发布。

      XHTML 指可扩展超文本标签语言。
  
      XHTML 是 HTML 与 XML（扩展标记语言）的结合物。

     XHTML 包含了所有与 XML 语法结合的 HTML 4.01 元素。

   + **XHTML1.1：** 2001年5月31日发布。XHTML1.0是XML风格的HTML4.01。XHTML1.1主要是初步进行了模块化。

   + **XHTML2.0：**XHTML 2是一种通用的标记语言。但不及HTML5的冲击。XHTML 2的开发工作将于2009年底停止，而资源将用于推动HTML 5的进展。
  
    + **HTML5：**
      HTML5 是对 HTML 标准的第五次修订，其主要的目标是将互联网语义化，以便更好地被人类和机器阅读，并同时提供更好地支持各种媒体的嵌入。
    
      而HTML5本身并非技术，而是标准。它所使用的技术早已很成熟，国内通常所说的html5实际上是html与css3及JavaScript和api等的一个组合，大概可以用以下公式说明：HTML5≈HTML+CSS3+JavaScript+API。

  **注1** ：html5
    html5兼容html4，在h4的基础上多出了新的标签和规范。

    各大主流浏览器对 CSS3 和 HTML5 的支持越来越完善，但是面对的用户群体复杂，需要兼容的浏览器版本也比较多，所以h5的一些新标签和规范没有大范围使用。

      w3c: http://www.w3school.com.cn/html5/html_5_intro.asp

      新特性：https://www.cnblogs.com/greatluoluo/p/5714221.html

      h5的兼容：https://www.cnblogs.com/liuna/p/5505016.html

      https://www.cnblogs.com/zhangyongl/p/6154981.html

### 三.h5新标签和标签的语义化
  * **语义化标签**

    nav	表示导航

    header	表示页眉

    footer	表示页脚

    main	文档主要内容

    article	文章

   aside	主题内容之外

   footer	文档或者页的页脚

  **h4.0.1**

    ````
    <body>
    <!--头部start-->
    <div class="header">
        <!--导航start-->
        <ul class="nav">
            <li><a href="#">导航1</a></li>
            <li><a href="#">导航2</a></li>
            <li><a href="#">导航3</a></li>
        </ul>
        <!--导航end-->
    </div>
    <!--头部end-->

    <!--主体start-->
    <div class="main">
        <!--文章start-->
        <div class="article"></div>
        <!--文章end-->

        <!--侧边栏start-->
        <div class="aside"></div>
        <!--侧边栏end-->

    </div>
    <!--主体end-->

    <!--底部start-->
    <div class="footer"></div>
    <!--底部end-->
    </body>
    ````

  **h5**

    ````
    <body>
    <!--头部start-->
    <header>
        <!--导航start-->
        <nav>
            <a href="#">导航1</a>
            <a href="#">导航2</a>
            <a href="#">导航3</a>
        </nav>
        <!--导航end-->
    </header>
    <!--头部end-->

    <!--主体start-->
    <main>
        <!--文章start-->
        <article></article>
        <!--文章end-->

        <!--侧边栏start-->
        <aside></aside>
        <!--侧边栏end-->

    </main>
    <!--主体end-->

    <!--底部start-->
    <footer></footer>
    <!--底部end-->
    </body>
    ````

  * **新标签：** [http://www.runoob.com/html/html5-new-element.html](http://www.runoob.com/html/html5-new-element.html)

  **audio：**

   [http://www.runoob.com/tags/tag-audio.html](http://www.runoob.com/tags/tag-audio.html)

   <audio> 标签定义声音，比如音乐或其他音频流

  **video：**

    [http://www.runoob.com/tags/tag-video.html](http://www.runoob.com/tags/tag-video.html)

   <video> 标签定义视频，比如电影片段或其他视频流。

  **canvas：**

    [http://www.runoob.com/html/html5-canvas.html](http://www.runoob.com/html/html5-canvas.html)
  
   示例：[https://cybermap.kaspersky.com/cn/](https://cybermap.kaspersky.com/cn/)

    <canvas> 元素用于图形的绘制，通过脚本 (通常是JavaScript)来完成.

   <canvas> 标签只是图形容器，您必须使用脚本来绘制图形。


### 四.不同版本IE浏览器的兼容性写法

  [https://www.cnblogs.com/qiujianmei/p/7192481.html](https://www.cnblogs.com/qiujianmei/p/7192481.html)

  ````
  <!--[if IE]>用于 IE <![endif]-->

  <!--[if IE 6]>用于 IE6 <![endif]-->

  <!--[if IE 7]>用于 IE7 <![endif]-->
  <!--[if IE 8]>用于 IE8 <![endif]-->
  <!--[if IE 9]>用于 IE9 <![endif]-->
  <!--[if gt IE 6]> 用于 IE6 以上版本<![endif]-->
  <!--[if lte IE 7]> 用于 IE7或更低版本 <![endif]-->
  <!--[if gte IE 8]>用于 IE8 或更高版本 <![endif]-->
  <!--[if lt IE 9]>用于 IE9 以下版本<![endif]-->
  <!--[if !IE 8]> -->用于非 IE <!-- <![endif]-->
  ````

### 五.html文档类型声明！

  * **描述**

   它是指示 web 浏览器关于页面使用哪个 HTML 版本进行编写的指令。这样浏览器才能获知文档类型。
     
    http://www.w3school.com.cn/tags/tag_doctype.asp

  * **HTML5**

   <!DOCTYPE html>

  * **HTML4**

    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">


### 六.头部标签含义

  * **哪些头部标签？**

   meta / title / link / script

  * **meta**

   **1.**  设置页面的编码格式

     <meta charset=”编码格式” />	

      注：通常设为UTF-8（8-bit Unicode Transformation Format）是一种针对Unicode的可变长度字符编码，又称万国码。

   **2.** 设置页面的关键词

      <meta name=”keywords” content=”” >
      做搜索引擎优化

   **3.** 设置页面的描述

      <meta name=”description” content=”” >
    做搜索引擎优化

   **4.** 刷新页面/重定向

      <meta http-equiv="Refresh" content="5;url=重定向页面路径" />
      eq:http://www.w3school.com.cn/tiy/t.asp?f=html_redirect

  * **title**

   页面标题

  * **link**
   <link> 标签定义文档与外部资源的关系。
   <link> 标签最常见的用途是链接样式表（引入css）。

    ````
    <link rel="shortcut icon" href="//www.fanli.com/favicon.ico"> //页面的图标
    <link href="//static2.51fanli.net/static/home-css-v9257.css" rel="stylesheet">
    ````

  * **script**

    插入js文件(两种方式)

    ````
    <script src="//static2.51fanli.net/common/libs/jquery/jquery.min.js"></script>
    <script>
          //写js代码
    </script>
    ````

### 七.**常用标签**

  大致分为：行内标签和块标签

  块标签独占一行，宽度默认和父元素一致，可以直接设置高度和宽度。

  行内标签根据标签包含内容 的宽高决定自己的宽高，无法设宽高。

  **块标签代表** ：div

  **行内标签代表** : a

### 八.**cookies和localStorage和sessionStorage的区别**

  https://www.cnblogs.com/jacobb/p/6824838.html

  * **对比**

    1. cookie数据始终在同源的http请求中携带（即使不需要），即cookie在浏览器和服务器间来回传递；

    而sessionStorage和localStorage不会自动把数据发送给服务器，仅在本地保存。cookie数据还有路径（path）的概念，可以限制cookie只属于某个路径下 

    2. **存储大小限制也不同**

    cookie数据不能超过4K，同时因为每次http请求都会携带cookie、所以cookie只适合保存很小的数据；

    sessionStorage和localStorage虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大 。

    3. **数据有效期不同**

    sessionStorage：仅在当前浏览器窗口关闭之前有效；

    localStorage：始终有效，窗口或浏览器关闭也一直保存，因此用作持久数据；

    cookie：只在设置的cookie过期时间之前有效，即使窗口关闭或浏览器关闭。

  * **操作**

   cookie:

    `document.cookie="name=jiang"//设置cookie`

    `var name = document.cookie//取cookie`

  sessionStorage： 

    `sessionStorage.setItem('name','jiang');//设置sessionStorage`

    `sessionStorage.getItem('testKey');//取值`

    `sessionStorage.removeItem("name")//删除`

  localStorage：

    `localStorage.setItem("name","jiang")//设置`

    `localStorage.getItem("name")//取值`

    `localStorage.removeItem("name")//删除`

### 九.生成html结构代码快捷键

  不同编辑器效果不同

  * **！+ tab**

  * **html: + tab / html:5 + tab*!

