## 业务相关综合分享


### 1.关于html模版添加class和ID的规范

* **class**

样式相关：中划线链接

```<div class="pro-list" ></div>```

js逻辑相关：J开头，下划线链接

````<div class="J_pro_list" ></div>````

* **id**

J开头，下划线链接

````<a id="J_click_btn" href="">````

>注：在修改模版时，J开头下划线链接的class名不要轻易改动，可能会引起js报错


### 2.埋点

* **链接发埋点：**

html :
 ````<a href="url?spm=..."></a>````
 
js :
```` window.location.href='url?spm=...'````

* **ubt发埋点**

html : 
 ````<a href="url" data-spm=".."></a>````
 
js :
 ````ubt.track(''....")````
 
### 3.曝光

* **UBT.PlugIns.Exposure.init();**

wiki:http://wiki.office.51fanli.com/wiki/Fe%EF%BC%9A%E9%83%A8%E7%BD%B2%E6%9B%9D%E5%85%89

````<img class="lazy " src="" data-expo="" alt="">````
````<img class="J_need_exposure " src="" data-expo="" alt="">````

* **UBT.track()**

配合js事件使用:
"common_baoguang" + userId + 该位置的曝光埋点

````
var expo= "page-page_nameh5~module-spikebg~zc-***~pid-***~std-54796";
UBT.track('common_baoguang', 'prouserid'.getCookie() || 'ZYSCUSERID'.getCookie() || '[userid]', expo,  "evttype=exposure");

````

### 4.新开页面(新开webview)的几种方式

* **当前页面打开的两种方式**

html：

````<a class="clear-desc" href="Url" >````

js：
`
window.location.href="urlLink";
`

* **通过html属性和js配合**

引入js: "//webapp/js/common/hybridapi/nativefunction.js"

````       <a class="clear-desc" target="newwebview" href="{$zc.zcUrl}" >````

js会遍历页面内的所有a标签，发现有这个newwebview属性的，就包ifali跳转，从而新开页面。

* **通过js跳转**

ifanli跳转

````Fanli.Utility.bridgeApp('ifanli://m.51fanli.com/app/show/web?url='');````

* **新开页面相关参数**

wiki链接：http://wiki.office.51fanli.com/wiki/Ifanli://m.51fanli.com/app/show/web
  1.禁止下拉刷新: rf=32
  2.禁止native导航: nonav=1&noback=0
> 注：参数是加在ifanli协议上的，不是加给页面链接。

````ifanli://m.51fanli.com/app/show/web?nonav=1&noback=0&url=''````


### 5.css的几个常用属性

* **display：定义建立布局时元素生成的显示框类型**

文档链接：http://www.w3school.com.cn/cssref/pr_class_display.asp
大致分为三个类型：行内元素/内联元素(inline)、块元素(block)、行内块元素(inline-block)、隐藏(none)

区别：
1.行内元素(inline)无法设置宽高，内容多大就占据多大的空间；
2.块元素(block)可以设置宽高，如果不设置宽高，默认宽度等于父元素的宽度，高度等于内容的高度；
3.行内块元素(inline-block)，可以设置宽高，不设置宽高和行内元素一致，设置场景为，多个行内元素需要设置宽高，但是又要并排展示。
> 注：html的行内元素和块元素的标签：https://www.cnblogs.com/yxm440/p/7667539.html

* **position：元素的定位类型**

文档链接：http://www.runoob.com/cssref/pr-class-position.html
大致分为三个类型：固定定位(relative)、相对定位(absolute)、绝对定位(fixed);
值：top、bottom、right、left；

定位区别：relative相对于自己的位置定位，在标准流中；absolute相对于有设置定位的父级元素定位，脱离标准流；fixed相对于浏览器定位，脱离标准流。


> 应用场景：

reletive常用于给相对定位的子元素做基准；

absolute做布局使用，可以不在乎其他元素的位置和大小，任意定位在父元素的任意位置；

fixed用于定位在浏览器的指定位置，页面滚动，他不动，例如滚动吸顶的tab栏和定位在浏览器底部的导航栏


* **z-index：定位元素的层级**

由于大部分定位元素脱离标准流，不占dom的位置，可以‘漂’在页面的任意位置，这样就有可能发生层叠覆盖，如果不做任何设置，在html中靠下的元素比前边的元素层级要高，会覆盖前边在同一位置定位的元素。

现在我们需要让指定的定位元素优先展示，就需要设置z-index，z-index值越高的元素层级越高，就会覆盖层级底的元素。

* **color**

颜色，这里主要讲的颜色值的几种格式的写法，background-color/border-color同样适用。

**英文名称**

color:red;
因为色值单一，很少在实际项目中使用。

**十六进制值写法**

color:\#000000;(黑色)、color:\#ffffff;(白色)
黑色和白色是两个极端的色值

**rgb**

color:rgb(0, 0, 0);、color:rgb(255, 255, 255);
同样是黑色和白色的两个写法

**rgba**

color:rgba(0, 0, 0, 0.5); 、color:rgba(255, 255, 255, 0.5);
比rgb格式多一个参数，前边三个色值，和rgb含义一样，最后一个值是透明度。
透明度的值是0-1，值越小，透明度越大，0是完全透明，1是完全不透明。

> 注：rgb和十六进制写法效果一样，但是十六进制写法更加简单，一般采用十六进制的写法；当遇到有透明度的时候，会采用rgba的写法。

### 6.css--盒子模型

* **刨析图**
![盒子模型结构图1](https://upload-images.jianshu.io/upload_images/7525071-ff00c1c3874bf091.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![盒子模型结构图2](https://upload-images.jianshu.io/upload_images/7525071-d4fbbf261dfd6192.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* **包含属性(由外到内)：margin、border、padding**

其中border和padding是算在元素的宽高内的，margin是为了撑开当前元素和周围元素的间距(不算元素的宽高)。

* **margin**

用于控制块与块（可以理解成块级元素）之间的距离。
top、right、bottom、left四个值。

**写法：**

margin: 2px;   (top = right = bottom = left = 2px)

margin: 2px 3px; (top =  bottom = 2px; right = left = 3px)

margin: 2px 3px 4px; (top = 2px  bottom = 4px; right = left = 3px)

margin: 2px 3px 4px 5px; (top = 2px; right = 30px;  bottom = 4px; left = 5px)

margin-top: 2px; margin-right: 3px; margin-bottom: 4px; margin-left: 5px; 


* **padding：**

用于控制元素所有内边距的宽度，元素与border之间的间距
top、right、bottom、left四个值。

**写法：** 同margin

* **border**

**元素的边框**

top、right、bottom、left四个值；border-width(宽度)、border-color(颜色)、border-style(样式)三个属性。

**写法：**

border: 1px solide #000;(1px宽，颜色为黑色的实线边框，四个方向都是相同的)
border-top:1px solide #000 ;(原始顶部设置1px宽，颜色为黑色的实线边框)

**border-style：**

文档链接：http://www.w3school.com.cn/cssref/pr_border.asp
常用样式：solide(实线)、dotted(点状线)、dashed(虚线)
![](https://upload-images.jianshu.io/upload_images/7525071-37ae6905ebcd12cc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 问题：
1.margin和padding的区别？margin和padding的使用场景？


### 7.static调用方法

* **static中的路径**

每个项目的static路径统一写在/static/static/groups路径下的PHP文件中。
![](https://upload-images.jianshu.io/upload_images/7525071-c423b3cc30e92c6f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

````
'9-index-css' => array(
		"//common/css/base.css",
		"//common/css/module/topbar.css",
		"//common/css/module/header-v2.css",
		"//common/css/module/faq.css",
		"//common/css/module/footer.css",
		"//common/css/ui/popup-v2.css",
		"//common/css/ui/button.css",
		"//common/css/ui/pagination.css",
		"//9/css/index.css",
		"//9/css/search.css",
	),

	'9-index-js' => array(
		"//common/js/fanli/debug/fanli.stacktrace.js",
		"//common/js/base.js",
		"//common/js/fanli/trace/ubt.js",
		"//common/plugins/placeholder/jquery.placeholder-min.js",
		"//common/plugins/autocomplete/jquery-ui-autocomplete-min.js",
		"//common/plugins/infinitescroll/jquery.infinitescroll-min.js",
		"//common/plugins/sidebar/jquery.sidebar-min.js",
		"//common/plugins/sidebar/jquery.sticky-min.js",
		"//common/plugins/lazyload/jquery.lazyload-min.js",
		"//common/libs/tools/overlay.min.js",
		"//common/libs/tools/expose.min.js",
		"//common/js/module/search.js",
		"//common/js/module/topbar.js",
		"//common/js/module/header-v2.js",
		"//common/js/module/footer.js",
		"//common/js/module/adloader.min.js",
		"//passport/js/function/showsignuppop.js",
		"//9/js/index.js",
		"//common/js/module/analytics.js",
	),

````

* **php按照路径取static**

1. 在html模板中

````
<?php
    $title = "小优街（原9块9包邮）";
    $cssList = array('/static/9-h5-index-css.css');
    $jsList = array('/static/9-h5-index-js.js');
?>
<include file="$header" remwidth="750" remswitch="1" />
html结构
<include file="$footer" />
````

2. 在PHP的action文件夹中
/模板项目根目录(super/tuan/······)/Lib/Action/路径下的php文件，读取模板配置信息中的pagename对应的路径配置信息，然后再到common/config_page.php中去找对应的static路径信息。
以/super/h5/bounty项目为例:
![](https://upload-images.jianshu.io/upload_images/7525071-77fffe5e1856fb04.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

````
  public function index() {
        $gaea = fsdk_gaea(self::GAEA_STORY_NUM);
        $this->assign('title', $gaea['title'][0]['data1']);
        $this->assign('useZepto', false);
        $this->assign('useVue', true);
        $this->assign('useLsCache', true);
        $this->assign('pagename', 'bounty-h5-index');
        $this->display();
    }
````

读取到pagename的信息，去查找config_page.php中的static路径：

````
return array(
  'PAGECSS' => 
  array (
		'bounty-h5-index' => '/static/super-h5-bounty-index-css.css',
		'bounty-h5-detail' => '/static/super-h5-bounty-detail-css.css',
		'hub-h5' => '/static/super-h5-hub-css.css',
	),
````

拿到对应的路径信息，可以到static/static/groups中去找具体的static文件信息了。


**html在线编辑器**

* https://c.runoob.com/front-end/61
* https://runjs.cn/code

