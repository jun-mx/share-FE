## css

* **含义**

CSS 指层叠样式表 (Cascading Style Sheets)

* **作用**

定义HTML的展示样式

* **引入方式**
 
 1. 内联式
  
  `<div style="width: 100px; height: 60px; background: red; font-size:20px;color: #fff; line-height: 60px; text-align: center;">内联样式</div>`
  
  2. 嵌入式引入
  
 ![](https://upload-images.jianshu.io/upload_images/7525071-7a88b93a10a06fea.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
 
 3. 外部式引入

`<link rel="stylesheet" href="index.css">`

**注：** 引入方式不同优先级不同
   
* **选择器**

[http://www.w3school.com.cn/cssref/css_selectors.asp](http://www.w3school.com.cn/cssref/css_selectors.asp)
在 CSS 中，选择器是一种模式，用于选择需要添加样式的元素。主要用在嵌入式和外部引用式中。
下边介绍常用选择器：
   1. 元素选择器---标签选择器
最常见的css选择器当属元素选择器了，在HTML文档中该选择器通常是指某种HTML元素，例如：p, h2, span, a, div乃至html。

`div { width: 100px;}`
`p {font-size: 30px; backgroud-color: gray;}`

   2. 类选择器
就是我们常见的class选择器，通过给多种不同的元素设置类名，然后给该类名设相应的样式，类名前加''.''。

` .calss-name {font-size: 30px; backgroud-color: gray;}`

   3. ID选择器
ID选择器和类选择器有些类似，但是差别又十分显著。首先一个元素只能拥有一个唯一的ID属性。其次一个ID值在一个HTML文档中只能出现一次，也就是一个ID只能唯一标识一个元素(不是一类元素，而是一个元素)。

`  <div id="id-name">ID选择器</div>  `
` #id-name {font-size: 30px; backgroud-color: gray;}`

   4. 属性选择器
属性选择器在css2中引入，使我们可以根据元素的属性及属性值来选择元素。

`<a href="xxx" title="xxx"></a>`
`a[href][title] { ...}//拥有href属性和title属性的a标签`

   5. 派生选择器
派生选择器，乍一看名字不知所云，它又名上下文选择器，它是使用文档DOM结构来进行css选择的。
![](https://upload-images.jianshu.io/upload_images/7525071-f42ed83f4d97c03e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
   
 * 包括：后代选择器、子元素选择器等等。
    
`ul li{ width: 100px;}`

`ul>li{ width: 100px;}`


* **css的优先级**

当选择器作用在标签上的时候，是存在优先级的
继承 < 通配符 < 标签选择器  <  class选择器  <  id选择器 < 行内样式 <  !important

` * {color: red;} //给全局添加阳=样式`

` .xxx {color: red!important;} //给制定选择器添加样式`
 
**注1：**  权重可以叠加

**注2：**  通常在控制台显示样式越靠上，证明优先级越高

## css3
* **简介：** 最新的css标准

* **前缀**
CSS3为我们提供了很多让人兴奋的新样式,由于浏览器的兼容性问题,有一些样式并不能很好的支持 不过这并不影响我们学习以及使用它

  **1. 原因：** 浏览器厂商在实现CSS3的效果时,有的还有的还在测试阶段,为了保证显示效果,我们在使用某些属性的时候需要添加额外的前缀；
这些浏览器引擎前缀(Vendor Prefix)主要是各种浏览器用来试验或测试新出现的CSS3属性特征。可以总结为以下3点：

    * 试验一些还未成为标准的的CSS属性——也许永远不会成为标准
    
    * 对新出现的标准的CSS3属性特征做实验性的实现
    
    * 对CSS3中一些新属性做等效语义的个性实现

  **2. 示例** ----属性xxx
  
  -ms-xxx:  ie浏览器
  -moz-xxx:  FireFox浏览器
  -o-xxx:  Opera浏览器
  -webkit-xxx:  Chrome以及Safari

  **3. 主流浏览器内核**
  Trident内核(IE)： 前缀为 -ms
  Gecko内核(FireFox)： 前缀为 -moz
  Presto内核(Opera)： 前缀为 -o
  Webkit内核(Chrome,Safari)： 前缀为 -webkit

* **颜色渐变**
1. 线性渐变

`background-image: linear-gradient(方向,开始颜色 开始位置 ,颜色2 开始位置,颜色3 开始位置.....);`


2. 径向渐变

`background:radial-gradient(半径  ,颜色1,颜色2等等);`

* **阴影**

`text-shadow: x偏移值,y偏移值,阴影模糊程度,阴影颜色;`

* **动画**

**@keyframes** :  制定动画内容

`@keyframes animationname {动画内容}`

**animation**: 

使用动画 动画的使用 需要通过animation这个属性,他是一个复合属性,但是再添加子属性时,除时间外,顺序可以打乱

[http://www.w3school.com.cn/cssref/pr_animation.asp](http://www.w3school.com.cn/cssref/pr_animation.asp)

**完整属性:**

    `动画名:animation-name: go; `
   
   `持续时间
    animation-duration: 1s;`
  
  `动画播放完毕时的状态 (还原,结束值)
    animation-fill-mode: forwards;`
  
  ` 延迟时间
    animation-delay: 1s;`
  
  ` 动画次数(具体次数,或者无限次)
    animation-iteration-count: infinite;`
  
  `动画的播放过渡类型
    animation-timing-function: ease-in;`
   
   `动画状态 running 或者pause
    animation-play-state: running;`
   
   `规定是否应该轮流反向播放动画
    animation-direction: alternate;`

   `animation: name duration timing-function delay iteration-count direction;`

