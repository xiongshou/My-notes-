

# 前端开发相关概念

1. 所有的浏览器对同一个CSS样式的解析都相同，因此页面在不同浏览器下的显示效果不一定相同
2. URL（英文Uniform Resource Locator的缩写）中文译为“统一资源定位符”。URL其实就是Web地址，俗称“网址”。
3. HTTP”是一种详细规定了浏览器和万维网服务器之间互相通信的规则。

# 头部相关标签基本概念

1. title标签设置的标题可作为默认快捷方式或收藏夹的名称
2. link标签
   1. href设置外部文档的地址
   2. rel设置当前文档与引用的外部文档的关系
   3. type设置外部文档的类型。
3. 如果设置页面刷新、失效期等元信息，可对meta标签添加相应的name属性。（错误）name搜索引擎属性

## meta标签

1. 单标签

   1. 对页面进行设置的格式：`<meta http-equiv="名称"content="值"/>`
   2. 对搜索引擎进行设置的格式：`<meta name="名称" content="值"/>`

2. ```html
   <!DOCTYPE html>
   <html>
    <head>
     <meta charset="utf-8"/>
     <!-- ********* Begin ********* -->
   
       <title>设置元信息</title>
       <meta http-equiv = "Refresh" content="10;Url = https://www.baidu.com/"/>
       <meta http-equiv = "Expires" content="Fir,31 Dec 2021 08:00:00 GMT"/>
       <meta name="keywords" content="前端,元信息,网页跳转,失效期,搜索关键词"/>
      
     <!-- ********* End ********* -->
    </head>
    <body>
     <h1 align="center">元信息的设置</h1>  
    </body> 
   </html>
   ```



# 标签

## 文本控制类标签

1. 块级元素：<hi> \ <p>\ <div>
2. 文本修饰类标签：行内元素\<span>
3. 显示内容的大小和浏览器默认文本的大小基本相同的是:h4
4. 空格字符： &nbsp;
5. div可以包含任何标签、行内元素不能包含块级元素
6. align 对齐方式：
   1. left:左对齐
   2. center:居中对齐
   3. right:右对齐
   4. justify:两端对齐
7. 水平线标签：<hr size = "3" width = "400" color = "blue" noshade>  



## 图像标签

1. 图像格式：jpg、png、gif
2. 绝对路径、相对路径
3. 网页背景图：background
4. 网页中嵌入图像img
5. title是页面标题、不是网页标题
6. href不是img属性
7. image属性
   1. src ：给定图像来源的位置
   2. alt ：设置在图像未载入前图片位置显示的文字
   3. Width和 height ：设定图像的宽度和高度
   4. title：鼠标停留在图片上时显示的说明文字

## 超链接标签

1. 链源：引起跳转的原因
2. 链宿：要跳转的目标
3. < a href="链宿">链源< /a>
4. _blank:在新窗口打开被链接文档
5.  < a href=" https://www.baidu.com/">这是一个指向百度页面的链接</a>
6. 图片链接百度网站：链接双标签<a>里面放一个  <img>单标签
7. 打开或下载音乐：直接<a>里面放
8. 页内链接
   1. 锚点位置：< a name = "Q">这是第7个网页</a>
   2. 点击的位置：< a href="#Q">查看第7个网页</a>



# 表格基本结构

## 基本概念

1. 表格结构：表格标题、项目表头、数据资料
   1. table：定义一个表格
   2. caption：定义表格标题
   3. tr：定义表格一行
   4. th：定义表头单元格
   5. td：定义表格中数据单元格
2. 定义项目表头的标签：<th>
3. 表格背景颜色：<bgcolor>
4. 定义表格中的行：tr
5. 定义表格标题：caption
6. 表格中文本对齐：th：middle

## 选择题

1. 设置表格内部框线属性：rules
2. 表格外部显示上下俩条边框线：frame取值：hsides
3. 表格内部框线只显示行线：rules取值：rows
4. 合并俩个水平方向单元格：colspan
5. rules=cols:只显示列与列的分割线



## HTML5音频相关的内容

1. HTML5支持的音频格式：WAV 、MP3 、 Ogg
2. audio元素常见属性
   1. src:地址
   2. controls：添加控件：播放，暂停、音量调节控件
   3. autoplay：自动播放
   4. loop：循环播放
   5. preload：加载方式
      1. none：不加载
      2. auto：自动加载
      3. metadate：元数据
3. source元素，媒体元素
   1. src：规定要播放的音频文件地址
   2. type：规定媒体资源MIME类型
4. 选择题
   1. 可以为同一个媒体数据指定多个播放格式与编码方法的标签是（source）
   2. audio元素中的src作用是（设置要播放音频的URL）
   3. 给audio标签添加auto属性，可以使得音频就绪好马上播放（错误）



## 视频相关的概念

1. 支持的视频格式
   1. MP4
   2. WebM
   3. Ogg
2. 常见属性：和音频差不多，外加width、height
3. 选择题
   1. H5不支持的格式：flv
   2. 用于播放H5的文件是：vidio
   3. mp4是safari浏览器支持的vidio视频文件格式
   4. load不属于vidio元素的属性
   5. autoplay属性可以实现视频加载

## CSS基础知识

1. 浏览器css3前缀
   1. -ms-：IE浏览器前缀
   2. -moz-：火狐浏览器
   3. -webkit-：苹果、微软、谷歌浏览器前缀
   4. -o-：欧朋浏览器前缀
2. CSS样式：选择器+声明
3. 引入CSS样式的方法
   1. 内联式：style属性
   2. 内嵌式：
   3. 外链式：.css文件
   4. 外导式
4. 选择题
   1. CSS值得是：Cascading Style Sheets
   2. 火狐浏览器：-moz-
   3. style属性定义内敛样式
   4. 外链式：link



# 题库

## 单元测试1

* 所有的浏览器对同一个CSS样式的解析都相同，因此页面在不同浏览器下的显示效果完全一样。（❌）

* URL（英文Uniform Resource Locator的缩写）中文译为“统一资源定位符”。URL其实就是Web地址，俗称“网址”。（对）
* “HTTP”是一种详细规定了浏览器和万维网服务器之间互相通信的规则。（对）
* 在网站建设中，JavaScript用于搭建页面结构。（错：是运行在浏览器中的解释型编程语言，
* 下面的选项中，关于Web标准说法正确的是（C、D）
  * A Web标准只要包括HTML标准
  * B Web标准是由浏览器的各大厂商联合制定的
  * C Web标准并不是某一个标准，而是一系列标准的集合
  *  D Web标准主要包括结构标准、表现标准和行为标准三个方面

## 单元测试2

---

### 文档结构

```html
<!DOCTYPE html>
<html>
  <head>
    <title>标题</title>
  </head>
  <body>
  </body>
</html>
```

### 文本控制标签

```html
<h1>一级标题</h1>
<p>
  段落标签
</p>
<br>换行标签
<hr>水平线标签
```

### 字形标签

```html
<b>粗体标签</b>
<i>斜体标签</i>
<u>下划线标签</u>

```

### 其他

```html
<img src="路径" width=“” height=“”> 插入图片
<a href=URL>**</a> 插入超链接
<a href=""></a>可以电子邮件链接、下载链接
链接到一个锚点
<a href="#c5"></a>设置锚点
<a name="c5"></a>跳转锚点
```

### 表格

```html
表头：th,表行tr，表列td
<table>
  <tr>
    <th></th>
  </tr>
  <tr>
  	<td></td>
  </tr>
</table>
```

### link标签





---



1、位于HTML文档的最前面，用于向浏览器说明当前文档使用哪种 HTML 或 XHTML 标准规范的标记是（  ）。

· A <!DOCTYPE>

· B <head></head>

· C <title></title>

· D <html></html>

标准答案：A

2、在HTML中，网页要显示的主体内容应放置在（  ）

· A <title></title>标记之间

· B <head></head>标记之间

· C <body></body>标记之间

· D HTML中的任意位置

标准答案：C

3、若要以加粗宋体、12号字显示“vbscript”以下用法中，正确的是（  ）。

· A <b><font size=12>vbscript</b></font>

· B <b > <font face= "宋体" size= 12> vbscript</font> < / b >

· C <b><font face=“宋体”size=12>vbscript</b></font>

· D <b><font face="宋体" fontsize=12>vbscript</b></font>

标准答案：B

4、下列属性中，哪一项是用于设置鼠标悬停在图像上时的提示文字？（  ）

· A title  ：网页、图像的标题、悬提文字

· B alt  : 替代文字，图片加载不出来用的

· C width

· D height

标准答案：A

5、<hr noshade>表示（ ） // hr：水平线

· A 表示水平线没有阴影

· B 表示水平线没有边框

· C 表示页面边界没有阴影

· D 表示水平线不显现

标准答案：A

6、下列说法错误的是（ ）

· A <sup></sup>表示上标

· B <em></em>表示下划线  ： <u> </u> 下划线

· C <s></s>表示删除线

· D <strong></strong>表示粗体

标准答案：B

7、在HTML中，(  )不是链接的目标窗口属性。

· A self

· B new

· C blank  ： // 新窗口

· D top： // 整个窗口打开

标准答案：B

8、图像文件名为myhome.jpg，要访问目标网站为http://www.edu.cn，以下创建一个以图像为链源的超链接正确是（ ）

· A <a href="http://www.edu.cn" >myhome.jpg</a>

· B <a href="http://www.edu.cn" ><img src="myhome.jpg"></a>

· C <img src="myhome.jpg"><a href="http://www.edu.cn" ></a>

· D <a href="http://www.edu.cn" ><img src="myhome.jpg"></a>

标准答案：B

9、以下创建E-mail链接的方法，正确的是（ ）

· A <a href="master@163.com" >管理员</a>

· B <a href="#master@163.com" >管理员</a>

· C <a href="callto:master@163.com" >管理员</a>

· D <a href="mailto:master@163.com" >管理员</a>

标准答案：D

10、定义表格的项目表头的HTML标签是（ ）

· A <table>

· B <td>

· C <tr>

· D <th>

标准答案：D

11、设置表格的边框为0的HTML 代码是（ ）

· A <table cellspacing=0>

· B <table height=0>

· C <table boeder=0>

· D <table cellpadding=0>

标准答案：C

12、<table rules=cols>，表示（ ）// cols行，row列

· A 显示所有分隔线

· B 只显示组(Groups)与组之间的分隔线

· C 只显示行与行之间的分隔线

· D 只显示列与列之间的分隔线

标准答案：D

13、<table frame=hsides>只显示一个边框。(   )

· A 对

· B 错

标准答案：B

> 边框相关知识
>
> frame：外边框属性；above上边框。below下边框。hsides上下边框。vsides左右边框。border上下左右边框。lhs左边框。rhs右边框。
>
> rules：内部边框属性；all全部内边框。none不显示边框。rows就显示行。cols就显示列。
>
> 水平合并colspan，垂直合并rowspan



14、图像文件和html文件位于同一文件夹，相对地址为<img src="logo.gif" />。(   )

· A 对

· B 错

标准答案：A

15、代码“<td rowspan="3">海淀区</td>”表示的意思是将水平方向的三个单元格合并为一个单元格。(  )

· A 对

· B 错

标准答案：B

> 相关内容。
>
> 表头th，表行tr，表列td
>
> rowspan行合并，三个行合并起开

 

单元测试3

1、下列选项不属于HTML5文档的结构元素是（  ）。

· A <article>

· B <header>

· C <font>

· D <aside>

标准答案：C

> Html5:header页眉，nav导航，article主页面区，aside次要信息区，footer页脚

2、HTML5 的全局属性中"contenteditable" 用于（  ）。

> 全局属性
>
> Hidden属性：规定元素不显示
>
> spellcheck：是不是对元素进行拼写和语法检查
>
> scontenteditable：是不是可以编辑
>
> contextmenu：右键上下文菜单

· A 规定元素的上下文菜单,该菜单会在用户点击右键点击元素时出现

· B 规定元素内容是否是可编辑的

· C 从服务器升级内容

· D 返回内容在字符串中首次出现的位置

标准答案：B

3、在HTML5 中，spellcheck 是（  ）。

· A 全局属性

· B HTML元素

· C 事件属性

· D 样式属性

标准答案：A

4、在HTML5中，下列用于展现页面中某个事物完成的进度的元素是（  ）。

· A details

· B meter

· C command

· D progress

标准答案：D

5、为了使得元素可拖动，可以把（ ）属性设置为ture。

· A draggable

· B contenteditable

· C editable

· D dropzone

标准答案：A

6、以下哪个标记用来建立一个有序列表（  ）。

· A <ni>

· B <ul>

· C <ol>

· D <dl>

标准答案：C

7、在定义列表中，一对<dt></dt>标记可以对应多对<dd></dd>标记。

· A 对

· B 错

标准答案：A

8、在进行列表嵌套时，无序列表中只能嵌套无序列表。

· A 对

· B 错

标准答案：B

9、在无序列表中经常设置type属性，下列属于type属性值的是（ ）。

· A disc

· B circle

· C pointer

· D square

标准答案：ABD

> 可以设置disk、circle、square属性，无序列表
>
> dl元素，自定义列表
>
> ![image-20201216155011960](https://tva1.sinaimg.cn/large/0081Kckwly1glpqxa0r4vj30tg0be0w7.jpg)

10、关于定义无序列表的基本语法格式，以下描述正确的是（  ）。

· A <ul></ul>标记用于定义无序列表

· B <li></li>标记嵌套在<ul></ul>标记中，用于描述具体的列表项

· C 每对<ul></ul>中至少应包含一对<li></li>

· D <li>不可以定义type属性，只能使用CSS样式属性代替

标准答案：ABC



 

单元测试4

## 相关内容

* 表单的结构

  * action：接收处理表单数据的服务器程序的url地址
  * name：取名
  * method：表单数据的提交方式get||post

* input控件

  * text文本框
  * password密码框
  * radio单选按钮
  * checkbox复选按钮
  * textarea多行文本框
  * 普通、提交、重置按钮

* textarea控件

* select控件

  * size：可见选项的数目
  * multiple：设定为多选
  * 搭配option

  ```html
  <form action="" methon="get">
    <select name="水果" size="3">
      <option value="apple" selected>苹果</option>
      <option value="peach">桃子</option>
    </select>
  </form>
        
  ```

## 正则表达式匹配

* . 匹配任何字符
* *匹配0或者多个它前面字符
* +匹配1或者多个前面字符
* ？匹配0或者1前面字符
* ^ 匹配字符串开始
* $匹配字符串结束

## 选择题

1、<form>与</form>之间的表单控件是由用户自定义的。下列选项中，不属于表单标记<form>的常用属性的是（  ）

· A action

· B size

· C method

· D name

标准答案：B

2、在HTML中，<form method=””>，method属性表示（  ）

· A 提交方式// get post

· B 表单所用的脚本语言

· C 提交的URL地址

· D 表单的类型

标准答案：A

3、在表单中插入单选按钮的HTML代码是（  ）

· A <input type="submit" >

· B < input type="button" >

· C < input type="reset" >

· D <input type=“radio”>

标准答案：D

4、在表单中插入文本域的正确的HTML代码是（  ）

· A <input type="password" size=15>

· B <textarea name="" rows="" cols=""> </textarea>

· C <select multiple><option value=""></select>

· D <input type="textarea" rows="" cols="" >

标准答案：B <textarea>起手

5、设置表单中密码框的最大长度为15正确的属性设置是（  ）

· A size=15

· B max=15

· C maxsize=15

· D maxlength=15

标准答案：D

6、下列能够实现列表框中选项为默认选项的<option>标记的属性是（  ）

· A value

· B size

· C selected

· D rows

标准答案：C

7、若要产生一个4行30列的多行文本域，以下代码中，正确的是（  ）

· A <input type="text" rows="4" cols="30" name="txtintrol">

· B <textarea rows="4" cols="30" name="txtintrol">

· C <textarea rows="4" cols="30" name="txtintrol"></ textarea >

· D <textarea rows="30" cols="4" name="txtintrol"></ textarea >

标准答案：C

8、在表单控件中，对复选框应用checked属性，指定默认选中项。

· A 对

· B 错

标准答案：A

9、在表单提交方式中，get方式的保密性好，并且无数据量的限制。

· A 对

· B 错

标准答案：B

10、代码<input type="text" id="txtAge" pattern="^[1-9]?[0-9]$"**>**可验证输入文本是否为1~9之间的数字。

· A 对

· B 错

标准答案：B



 

单元测试5

* audio：用于音乐文件与其他音频流的播放
* src：地址
* 三种音频格式：Ogg、MP3、WAV
* sudio标签的属性
  * autoplay
  * controls
  * loop
  * preload
  * src
* video：用于视频文件的播放
* 三种视频格式：Ogg、MPEG4、WebM

1、在HTML中，可以使用（  ）标记向网页中插入视频。

· A <src>

· B <path>

· C <video>

· D <audio>

标准答案：C

2、下列属性中指定媒体是否在页面加载后自动播放的是（  ）

· A 100p

· B autoplay

· C poster

· D auto

标准答案：B

3、下列选项中，属于audio元素的属性是（  ）

· A poster

· B width

· C height

· D preload

标准答案：D

4、下列选项中，（  ）不是HTML 5所支持的视频格式

· A WebM

· B Ogg

· C MP4

· D AVI

标准答案：D

5、可以通过（  ）元素来为同一个媒体数据指定多个播放格式与编码方式

· A source

· B video

· C audio

· D 以上都不是

标准答案：A







单元测试7

* 构造：选择符+声明（属性+值）
* 选择器
  * 通用选择器
  * 标签选择器
  * 类选择器
  * id选择器
  * 伪类选择器
  * 群组选择器
  * 派生选择器
  * 属性选择器
  * 组合选择器
* 应用css的4种方式
  * 内联式
  * 内嵌式
  * 链入式
  * 导入式
* css的特性
  * 继承性
  * 特殊性
  * 层叠性
  * 重要性

1、下列选项中，（  ）的CSS语法是正确的

· A body:color=black

· B {body:color=black(body)}

· C body{color:black;}

· D {body;color:black}

标准答案：C

2、当<p>标记内嵌套<strong>标记时，就可以使用后代选择器对其中的<strong>标记进行控制，下列写法正确是（   ）

· A strong p{color:red;}

· B p strong{color:red;}

· C strong,p{color:red;}

· D p.strong{color:red;}

标准答案：B

3、在内嵌式CSS样式中，<style>标记可以设置元素的样式，它一般位于（ ）标记中<title>标记之后

· A <h1>

· B <p>

· C <head>

· D <body>

标准答案：C

4、在CSS中，用于设置首行文本缩进的属性是（  ）

A text-decoration ：元素文本装饰

B text-align  ：设置对齐方式

C text-transform  ：转换不同元素中的文本

D text-indent  ：缩进

标准答案：D

5、如果使用内嵌式CSS样式表定义<p>标记字号为12像素，链入式定义<p>标记颜色为红色，那么段落文本将显示为（  ）

· A 只显示12像素

· B 12像素红色

· C 只显示红色

· D 以上都不正确

标准答案：B

6、内联式CSS样式是通过标记的（  ）属性来设置元素的样式

· A class

· B style

· C id

· D name

标准答案：B

7、下列选项中，用于设置鼠标悬停效果的超链接样式（  ）

· A a:hover{ font-size:16px; }  ：鼠标悬停

· B a:active{ font-size:16px; }  ：点击一个链接变成活动链接

· C a:visited{ font-size:16px; }

· D a:link{ font-size:16px; }

标准答案：A

> visited选择器设置访问过的页面链接的样式
>
>  hover选择器当有鼠标悬停在其上的链接样式，
>
> active 选择器设置当你点击链接时的样式。

8、id选择器使用（  ）进行标识，后面紧跟id名

· A ^

· B *

· C #

· D .

标准答案：C

9、text-decoration是文本修饰属性，其属性值（  ）是用来设置下划线的

· A line-through

· B overline

· C blink

· D underline

标准答案：D

10、在CSS中，去掉无序列表项前面的符号的方法是（  ）

· A ul{ list-style:none;}

· B ul{ list-style-type:none;}  : none!!!

· C ul{ list-type:no ;}

· D ul{ list-style-type :null;}

标准答案：B



 

单元测试8

1、下列设置“上边距：20px、下边距：30px、左边距：40px、右边距：50px”边距属性正确的是（  ）。

· A margin:20px 30px 40px 50px

· B border: 20px 30px 40px 50px

· C margin:20px 50px 30px 40px

· D margin-top:20px 30px 40px 50px

标准答案：C

2、行内元素也称内联元素或内嵌元素，其特点是，不必在新的一行开始，同时，也不强迫其他的元素在新的一行显示，下列选项中为行内元素的是（  ）。

· A <h1>

· B <span>

· C <div>

· D <ul>

标准答案：B

3、在CSS中，可以通过float属性为元素设置浮动，以下选项中不属于float属性值的是（   ）。

· A left

· B center

· C right

· D none

标准答案：B

4、将一个盒子的上边框定义为1像素、蓝色、单实线，下列代码正确的是（  ）。

· A border-top：1px solid #00f;

· B border：1px solid #00f;

· C border-top：1px dashed #00f;

· D border：1px dashed #00f;

标准答案：A

5、下列选项中，可以去掉列表的项目符号的是（  ）。

· A list-type:square

· B list-type:circle

· C list-type:no

· D text-decoration: none

标准答案：D

6、如果想将两个层排列在同一行中，下列描述不能实现的是（  ）。

· A 直接插入两个DIV标记，会自动排在同一行

· B 指定DIV的position属性为absolute,然后将层位置定位同一行

· C 指定DIV标记的宽，并且为它们指定浮动方式

· D 使用一个表格，将两个层分别放入一行中的两个单元格内

标准答案：A

7、在css中，如果要清除浮动层对文本的影响，下列说法正确的是（  ）。

· A 为浮动层增加clear属性，并设置其属性为both

· B 为浮动层增加clear属性，并设置其属性为none

· C 为放置文本的标签增加clear属性，并设置其属性为none

· D 为放置文本的标签增加clear属性，并设置其属性为both

标准答案：D

8、CSS中position:fixed表示（  ）。

· A 相对于浏览器窗口进行定位

· B 相对于它在原文档流的位置进行定位

· C 相对于其上一个已经定位的父元素进行定位

· D 相对于父元素进行定位

标准答案：A

9、在CSS中，为页面中的某个DIV标签设置样式div{width:200px;padding:0 20px;border:5px；}，则该标签的实际宽度为（  ）。

· A 200px

· B 220px

· C 240px

· D 250px

标准答案：D

10、将元素转换为行内块元素的方法是对其应用display:inline-block;样式。

· A 对

· B 错

标准答案：A

**
**

 

单元测试11

1、在下列（ ）HTML元素中放置Javasript代码。

· A <js>

· B <JavaScript>

· C <script>

· D <scripting>

标准答案：C

2、以下变量命名中，（ ）符合命名规则。

· A with

· B userName

· C a&bc

· D 8-depart

标准答案：B

3、解释执行JavaScript的是（  ）。

· A 服务器

· B 编辑器

· C 浏览器

· D 编译器

标准答案：C

4、在JavaScript中，所有数字都是数值型，并不区分整型数值和浮点型数值。（  )

· A 对

· B 错

标准答案：A

5、在JavaScript中，下列满足变量x大于等于20且小于100条件的正确表达式是（ ）  。

· A (X>=20 & x<100)

· B (x>=20 and x<100)

· C (X>=20 or x<=100)

· D (x>=20 && x<100)

标准答案：D

6、引用名为“xxx.js”的外部脚本的正确语法是（ ）。

· A <script src=”xxx.js”>

· B < script href=”xxx.js”>

· C <script name=”xxx.js”>

· D < script type=”xxx.js”>

标准答案：A

7、下列能向页面弹出告警消息框的JavaScript语句是（  ）。

· A “信息正确吗？”

· B <h4>信息正确吗？ </h4><br/>

· C document.write("信息正确吗？ ");

· D alert("信息正确吗？ ");

标准答案：D

8、下列选项中，JavaScript运算符的优先级最高的是（  ）。

· A +

· B ++

· C （）

· D = =

标准答案：C

9、下列代码中，用于判断当 i 不等于 5 时执行一些语句的条件语句是（  ）。

· A if =! 5 then

· B if <>5

· C if (i <> 5)

· D if (i != 5)

标准答案：D

10、下列声明自定义函数selectNumber()正确的是（  ）。

· A function : selectNumber(){}

· B function selectNumber(){ }

· C function =selectNumber(){}

· D function {selectNumber()}

标准答案：B



 

单元测试12

1、下列选项中，（ ）不是JavaScript中的内置对象。

· A Date

· B String

· C Array

· D List

标准答案：D

2、将字符串s中的所有字母变为小写字母的方法是（ ）。

· A s.toSmallCase()

· B s.toLowerCase()

· C s.toUpperCase()

· D s.toUpperChars()

标准答案：B

3、分析下面的JavaScript代码段：

  var a=15.49;

  document.write(Math.round(a));

  输出的结果是（  ）。

· A 15.4

· B 15.5

· C 15

· D 16

标准答案：C

4、在JavaSript中，可以使用Date对象的（  ）方法返回一个月中的每一天。

· A getDate()

· B getYear()

· C getMonth()

· D getTime()

标准答案：A

5、Array对象的（ ）方法可以使用颠倒数组中元素的顺序。

· A shift()

· B reverse()

· C splice()

· D slice()

标准答案：B

6、代码var count=Math.ceil(Math.random()*30)+90,count的值为（  ）。

· A 90<count<120

· B 90<=count<120

· C 90<=count<=120

· D 90<count<=120

标准答案：C

7、在JavaScript中，下列哪段代码能够在1秒之后执行表达式expression?(   )。

· A window.setTimeout(1000,expression);

· B window.setTimeout(expression ,1);

· C window.setTimeout(1 ,expression);

· D window.setTimeout(expression ,1000);

标准答案：D

8、如果今天是2018年9月29日，则下列JavaScript代码运行后，将在网页上显示（ ）。

   var now=new Date();

   var year=now.getYear();

   var month=now.getMonth();

   var date=now.getDate();

   document.write(year+””month+””+date);

· A 2018 09 29

· B 2018 9 29

· C 2018 08 29

· D 2018 8 29

标准答案：D

9、考察以下程序片段：

   var str="12px";

   var s=str.indexof(“2”）

   alert(s);

 以下选项正确的是（ ）。

· A 输出1

· B 输出2

· C 输出p

· D 输出12

标准答案：A

10、分析下面的JavaScript代码段

   a=new Array(2,4,4,5,6);

   sum=0;

   for(i=0;i<a.length;i++)

   sum+=a[i];

   document.write(sum);

  输出结果是（  ）。

· A 21

· B 23456

· C 2,3,4,5,6

· D 19

标准答案：A



 

单元测试13

1、下列JavaScript语句中，能实现单击一个按钮时弹出一个消息框的是（）。

· A <button value ="鼠标响应" onclick=alert("确定")></button>

· B <input type="button" value ="鼠标响应" onclick=alert("确定")>

· C <input type="button" value ="鼠标响应" onchange=alert("确定")>

· D <button value ="鼠标响应" onchange=alert("确定")></button>

标准答案：B

2、某网页中有一个窗体对象，其名称是mainForm，该窗体对象的第一个元素是按钮，其名称是myButton，表述该按钮对象的方法是（  ）。

· A document.forms.myButton

· B document.mainForm.myButton

· C document.forms[0].element[0]

· D 以上都可以

标准答案：B

3、下列选项中，（  ）不是网页中的事件。

· A onclick

· B onmouseover

· C onsubmit

· D onpressbutton

标准答案：D

4、HTML文档的树状结构中，（  ）标签为文档的根节点，位于结构中的最顶层。

· A <HTML>

· B <HEAD>

· C <BODY>

· D <TITLE>

标准答案：A

5、在HTML页面中包含一个按钮控件mybutton,如果要实现点击该按钮时调用已定义的Javascript函数compute，要编写的HTML代码是（  ）。

· A <input name=”mybutton” type=”button” onblur=”compute ()” value=”计算“>

· B <input name=”mybutton” type=”button” onfocus=”compute ()” value=”计算”>

· C <input name=”mybutton” type=”button” onclick=”function compute ()” value=”计算“>

· D <input name=”mybutton” type=”button” onclick=”compute ()” value=”计算”>

标准答案：D

6、Javascript中制作图片代替按钮的提交效果需要手动提交方法submit()，以下调用正确的是（  ）。

· A submit()

· B myform.submit()

· C document. myform.submit()

· D window. myform.submit()

标准答案：C

7、window的哪个方法可以弹出带文本输入框的对话框？（  ）

· A confirm()

· B alert()

· C prompt()

· D open()

标准答案：C

8、open()方法的哪个外观参数可以设置是否显示滚动条？（  ）。

· A location

· B menubar

· C scrollbars

· D toolbar

标准答案：C

9、setInterval(“alert(‘welcome’;”,1000);这条代码的意思是（  ）。

· A 等待1000秒后，再弹出一个对话框

· B 等待1秒后弹出一个对话框

· C 每隔1秒弹出一个对话框

· D 语句报错，语法有问题

标准答案：C

10、分析以下代码

<script>

 window.onload=function(){

var a=document.getElementById(‘mydiv’)；

alert(a.lastChild.previousSibling.innerHTML);

}

</script>

<dl id=”mydiv”

<dt>aaa</dt>

<dd>xxx</dt>

<dt>bbb</dt>

<dt>ccc</dt>

</dl>

弹出提示对话框的内容是     。

ccc

候选答案一：

ccc

候选答案二：

CCC

11、假设a.html和b.html在同一个文件夹下面，请在a.html页面中使用javascript代码实现：点击这个a.html中的“打开”按钮，弹出一个新窗口。该窗口宽500px，高度为450px，该窗口中显示的页面是b.html页面。写出实现该功能的HTML代码。

参考答案：
 ![IMG_256](/Users/xiongshou/markdown/课程/clip_image002.jpg)



 

综合测试

1、在HTML中，网页的标题内容应放置在（  ）。

· A <title></title>标记之间

· B <head></head>标记之间

· C <body></body>标记之间

· D HTML中的任意位置

标准答案：A

2、下列选项中哪一个属性不是文本的标签属性（  ）？

· A align

· B color

· C nbsp

· D face

标准答案：C

3、下列选项中，（  ）是换行符标记。

· A <enter>

· B <br>

· C <pre>

· D <font>

标准答案：B

4、定义表格行的HTML标签是（  ）。

· A <table>

· B <td>

· C <th>

· D <tr>

标准答案：D

5、以下创建E-mail链接的方法，正确的是（  ）。

· A <a href="master@163.com" >管理员</a>

· B <a href="#master@163.com" >管理员</a>

· C <a href="callto:master@163.com" >管理员</a>

· D <a href="mailto:master@163.com" >管理员</a>

标准答案：D

6、若要设置网页的背景图像为bg,jpg，以下标记中，正确的是（  ）。

· A <body background= "bg.jpg ">

· B <body bground= "bg.jpg ">

· C <body image="bg.jpg ">

· D <body bgcolor= "bg.jpg ">

标准答案：A

7、以下关于列表标记说法错误的是（  ）。

· A <ol>有序列表

· B <ul>无序列表

· C <li>嵌套列表

· D <dl>定义列表

标准答案：C

8、下列选项中，（  ）的CSS语法是正确的。

· A body:color=red

· B {body:color=red(body)}

· C body{color:red;}

· D {body;color:red}

标准答案：C

9、下列设置“上边距：20px、下边距：30px、左边距：40px、右边距：50px”边距属性正确的是（  ）。

· A margin:20px 30px 40px 50px

· B border: 20px 30px 40px 50px

· C margin:20px 50px 30px 40px

· D margin-top:20px 30px 40px 50px

标准答案：C

10、在HTML5中，下列用于展现页面中某个事物完成的进度的元素是（  ）。

· A details

· B meter

· C command

· D progress

标准答案：D

11、若要在当前网页中定义一个独立类的样式myText，使具有该类样式的正文为“Arial”，字体大小为9pt，行间距为13.5pt。以下定义方法中，正确的是（  ）。

·A <style> .myText{Font-Familiy :Arial ;Font-size :9pt ;Line-Height :13.5pt} </style>

·B <style> myText{Font-Familiy :Arial ;Font-size :9pt ;Line-Height :13.5pt} </style>

·C <style> .myText{FontName :Arial ;FontSize :9pt ;LineHeight :13.5pt} </style>

·D <style> myText{FontName :Arial ;FontSize :9pt ;LineHeight :13.5pt} </style>

标准答案：A

12、下列选项中，（  ）不是HTML 5所支持的视频格式。

· A WebM

· B Ogg

· C MP4

· D AVI

标准答案：D

13、CSS中position: relative表示（  ）。

· A 相对于浏览器窗口进行定位

· B 相对于它在原文档流的位置进行定位

· C 相对于其上一个已经定位的父元素进行定位

· D 相对于父元素进行定位

标准答案：B

14、引用外部compute.js脚本正确的语法是(  )。

· A <script href="compute.js">

· B <style href="compute.js">

· C <script src="compute.js">

· D <style src="compute.js">

标准答案：C

15、下列选项中，声明自定义函数selectNumber()正确的是（  ）。

· A function : selectNumber(){}

· B function selectNumber(){ }

· C function =selectNumber(){}

· D function {selectNumber()}

标准答案：B

16、下列选项中，（   ）是求出两个数最大数？

· A Math.ceil(20,50)

· B Math.max(20,50)

· C Math.min(20,50)

· D top(20,50)

标准答案：B

17、在JavaSript中，可以使用Date对象的（  ）方法返回月份值。

· A getDate()

· B getYear()

· C getMonth()

· D getTime()

标准答案：C

18、open()方法的哪个外观参数可以设置是否显示工具栏？（  ）。

· A location

· B menubar

· C scrollbars

· D toolbar

标准答案：D

19、下列选项中，（  ）可以表达方程X2=4中的上标“2”。

· A <b>2</b>

· B <tt>2</tt>

· C <sub>2</sub>

· D <sup>2</sup>

标准答案：D

20、分析下面的JavaScript代码段：

Var a=12.48;

Document.write(Math.round(a));

· A 12

· B 12.5

· C 12.4

· D 13

标准答案：A

21、下面的选项中，关于Web标准说法正确的是（   ）。

· A Web标准只要包括HTML标准。

· B Web标准是由浏览器的各大厂商联合制定的。

· C Web标准并不是某一个标准，而是一系列标准的集合。

· D Web标准主要包括结构标准、表现标准和行为标准三个方面。

标准答案：CD

22、在CSS中，下列选项（  ）属于BOX模型的属性。

· A font

· B margin

· C border

· D visible

标准答案：BC

23、以下（  ）内容是HTML文件头部内容所包括的。

· A 注释、表单域。

· B 网页标题、关键字。

· C 作者信息、网页描述、自动刷新。

· D CSS样式。

标准答案：BCD

24、下列选项中（  ）可以通过javascript的应用得以实现。

· A 交互导航

· B 表单验证

· C 简单的数据搜寻

· D 日期显示

标准答案：ABCD

25、下列选项中（  ）是javascript的全局函数？

· A escape

· B parseFloat

· C alert

· D eval

标准答案：ABD

26、Web开发技术包括客户端和服务器端的技术。

· A 对

· B 错

标准答案：A

27、当样式定义重复出现的时候，最先定义的样式起作用。

· A 对

· B 错

标准答案：B

28、在定义列表中，一对<dt></dt>标记只能一对<dd></dd>标记。

· A 对

· B 错

标准答案：B

29、代码“<td rowspan="3">万柏林区</td>”表示的意思是将水平方向的三个单元格合并为一个单元格。

· A 对

· B 错

标准答案：B

30、在表单提交方式中，post方式的保密性好，并且无数据量的限制。

· A 对

· B 错

标准答案：A

31、将字符串s中的所有字母变为小写字母的方法是s.toUpperCase()。

· A 对

· B 错

标准答案：B

32、解释并执行JavaScript的是服务器。

· A 对

· B 错

标准答案：B

33、setInterval(“alert(‘welcome’;”,1000);这条代码的意思是等待1000秒后，再弹出一个对话框。

· A 对

· B 错

标准答案：B

34、a:hover{ font-size:16px; }可用于设置鼠标悬停效果的超链接样式。

· A 对

· B 错

标准答案：A

35、<span>为行内元素。

· A 对

· B 错

标准答案：A

36、程序填空题（每空2分）

**按下图页面效果和代码中注释部分提示信息完善程序代码。**

<html> 

<head>

   <title> 标题字应用 </title>

</head>

<body>

​    （1）  **<!-- 3****号标题显示“web前端开发技术” -->** 

​    （2）  **<!****—水平线宽度：3，颜色：红色，对齐方式：居中 -->**

​    （3）  **<!-- 5****号标题显示“1.HTML” -->**

​    （4）   **<!-- 5****号标题显示“2.CSS ” -->**      

​    （5）  **<!-- 6****号标题显示“3.JavaScript ” -->** 

 </body>

</html>

![image](/Users/xiongshou/markdown/课程/clip_image003.jpg)

参考答案

![IMG_257](/Users/xiongshou/markdown/课程/clip_image005.jpg)

37、程序填空题（每空2分）

**按下图所示效果，参照注释提示信息，完成代码填充。**

![image](/Users/xiongshou/markdown/课程/clip_image007.jpg)

<html>

<head>

<title> 改变网页页面字的大小 </title>

<style type="text/css">

 \#content{

  **/\*****填充说明 （6）设置边框宽度2px、线型groove、颜色#0000cc \*/**

  font-size:12px;

line-height:200%;

padding:10px;

  background:#000099;

color:white;

（6）          ;}

  p{text-indent:2em;}

</style>

**<!****—填充说明：（7）设置type属性值；（8）通过ID获取元素方法；**

**（9）超链接的链宿属性；（10）设置单击事件句柄 -->**

<script type="  （7）                   ">

  function setfont(size){

   var obj=  （8）        ("content");

   obj.style.fontSize=size;

   obj.style.color="#ff0000";}

</script>

</head>

<body>

  <h2 align="center">用JavaScript代码改变网页字体大小</h1>

   <div>设定字体大小: &nbsp;&nbsp;<a   （9）                     ="javascript:setfont('12px')">小</a>&nbsp;&nbsp;

   <a href="#"   （10）                 ="javascript:setfont('18px');">中</a>&nbsp;&nbsp;

   <a href="javascript:setfont('24px');">大</a></div>

   <div id="content">

    <p>JavaScript是一种能让你的网页更加生动活泼的程式语言，也是目前网页中设计中最容易学又最方便的语言。</p> </div>

</body>

</html>

参考答案

![IMG_259](/Users/xiongshou/markdown/课程/clip_image009.jpg)

38、表单编程。

按照如下要求编程实现如图所示页面布局效果。

![image](/Users/xiongshou/markdown/课程/clip_image011.jpg)

 

（1）页面标题为“留言簿”；

（2）表单中添加1个文本框、1个密码框、1个文本区域、1个提交按钮、1个重置按钮，其中姓名文本框最大长度为10、密码框最大长度为15、文本区域为5行40列；

（3）用3号标题设置页面上的“留言簿”。

参考答案

![IMG_261](/Users/xiongshou/markdown/课程/clip_image013.jpg)

39、JavaScript编程

计算N!。按下图页面效果，并将N！结果输出到页面上。

![image](/Users/xiongshou/markdown/课程/clip_image015.jpg)

（1）采用while循环结构实现计算N！；

（2）用随机函数产生[1，10]任一正整数，并赋值给n；

（3）将计算结果直到输出在页面上；

（4）用4号标题设置“计算N！”；

（5）<script>放置在<body>中。

参考数学函数：round():四舍五入；floor():下舍入；ceil()：上舍入。

参考答案

![IMG_263](/Users/xiongshou/markdown/课程/clip_image017.jpg)



 

编程训练

1、按照以下要求编程实现如图所示表格。

（1）表格标题占表格一行并跨列居中；

（2）表格边框宽度为1；

（3）单元格内容水平居中，字体为“黑体”，必须用采用内部样式表定义。

![image](/Users/xiongshou/markdown/课程/clip_image019.jpg)

参考答案

![IMG_257](/Users/xiongshou/markdown/课程/clip_image021.jpg)

2、按照以下要求编程实现如图所示页面布局效果。

（1）页面标题为“注册页面”；

（2）表单中添加1个文本框、1个密码框、2个单选按钮、1个文本区域、1个提交按钮、1个重置按钮，其中姓名文本框最大长度为10、密码框最大长度为15、文本区域为10行40列；

（3）用3号标题设置页面上的“个人注册”；

![image](/Users/xiongshou/markdown/课程/clip_image023.jpg)

参考答案

![IMG_259](/Users/xiongshou/markdown/课程/clip_image025.jpg)

3、计算正方形的面积。

按下图页面效果，编程实现所需功能。

（1）表单中设置2个文本框、1个按钮、1个重置按钮，其中正方形的面积文本框设置为只读；

（2）编写两个自定义函数，分别是计算正方形的面积函数area（radius）、在页面上显示结果show()，并在show()函数中调用area(radius)函数；

（3）输入完正方形边长后，点击“计算”按钮后，将计算结果显示在“正方形的面积”文本框中；

（4）点击“重置”按钮后，将所有文本框清空；

![image](/Users/xiongshou/markdown/课程/clip_image027.jpg)

参考答案

![IMG_261](/Users/xiongshou/markdown/课程/clip_image029.jpg)

4、将一个摄氏温度值转换为一个华氏温度值，摄氏温度转换为华氏温度的公式为：华氏温度 = 9 / 5 * 摄氏温度 + 32。

按下图页面效果，编程实现所需功能。

（1）表单中设置2个文本框、1个“转换“按钮、1个”重置“按钮，其中华氏度文本框设置为只读；

（2）编写自定义函数show()实现温度转换及显示，用户在单击“转换“按钮时调用该函数；

（3）用户在摄氏度对应的文本框中输入数据后，点击“转换”按钮后，将计算结果保留2位小数并显示在“华氏度”文本框中；

（4）点击“重置”按钮后，将所有文本框清空；

![image](/Users/xiongshou/markdown/课程/clip_image031.jpg)

参考答案

![IMG_263](/Users/xiongshou/markdown/课程/clip_image033.jpg)

5、编写一个JavaScript程序，运用document.write（）显示当前时间及距离2019年元旦的天数。

请按下图页面效果，编程实现所需功能。

（1）当前时间now运用new Date()直接获取。

（2）目标时间nationalDay按照2019年1月1日0点0分0秒设置。

（3）运用系统内置函数parseInt（）将目标时间与当前时间相差的天数取整显示。

![image](/Users/xiongshou/markdown/课程/clip_image035.jpg)

参考答案

![IMG_265](/Users/xiongshou/markdown/课程/clip_image037.jpg)

6、运用CSS字体及文本样式属性，制作一个新浪博客首页的展示效果。具体要求如下： 

（1） 设置所有文本为微软雅黑、14像素、黑色字体。

（2） 设置“新浪”、“新浪网”为红色字体，“博客首页”为蓝色字体，网址及日期为绿色字体。

（3） 设置标题为16像素、左对齐、下划线的效果。设置文本“-百度快照-评价”为灰色、下划线的效果。

![image](/Users/xiongshou/markdown/课程/clip_image039.jpg)

参考答案

![IMG_267](/Users/xiongshou/markdown/课程/clip_image041.jpg)

7、通过无序列表和有序列表进行嵌套，实现一个三级列表效果，如下图所示。具体要求如下：

（1）定义无序列表。在对应的一级列表项中嵌套无序列表。

  （2）在二级无序列表的子列表项“绿茶”中嵌套有序列表。

![image](/Users/xiongshou/markdown/课程/clip_image043.jpg)

参考答案

![IMG_269](/Users/xiongshou/markdown/课程/clip_image045.jpg)

8、编程实现下图所示页面及功能，要求：

（1）页面包含一个下拉列表框、一个文本框和一个按钮，下拉列表框选择要去的网页，当选择完毕后文本框中出现对应的网页地址。单击确认按钮将跳访问文本框中出现的网页。

（2）下拉列表项包含：搜宝贝、逛商城、我的足迹、购物车；对应的网页分别为：1.html, 2.html, 3.html, 4.html。其中搜宝贝为默认选项。

![image](/Users/xiongshou/markdown/课程/clip_image047.jpg)

参考答案

![IMG_271](/Users/xiongshou/markdown/课程/clip_image049.jpg)

9、编写一个简易计时器程序。请按下图页面效果，编程实现所需功能。

（1）页面包含一个“开始”按钮，一个“暂停”按钮以及一个用于显示时间的文本框。

（2）当点击“开始”按钮时,调用函数timedCount()从 0 开始按秒计时，文本框显示实时的计时时间（以秒为单位）。

（3）当点击“暂停”按钮时，将停止计时，文本框显示的时间不再增加。

![image](/Users/xiongshou/markdown/课程/clip_image051.jpg)

参考答案

![IMG_273](/Users/xiongshou/markdown/课程/clip_image053.jpg)

10、按下图要求编程实现计算3+6+9+…+36的和。

（1）  采用For循环结构实现计算累加和；

（2）  分别输出参加计算的数，用空格分隔；

（3）  输出累加和，格式如“3+6+9+…+36=234”

![image](/Users/xiongshou/markdown/课程/clip_image055.jpg)

# 参考答案

![IMG_275](/Users/xiongshou/markdown/课程/clip_image057.jpg)

 



程序分析

1、根据注释的要求，补全代码。

<html>

  <head>

  （1）                         /*设置页面标题为“图像标签”*/

 </head>

  <body>

​    （2）                   /*将文字“插入图像”显示为3号子标题*/

 <img src="pic.jpg"

alt="这是一张插图"

width="200"  

height="200"

   （3）    /*设置3px的边框效果*/

 

（4）   /*设置鼠标悬停时显示" LOGO图片"的文本提示效果*/>

  </body>

</html>

参考答案

![IMG_256](/Users/xiongshou/markdown/课程/clip_image059.jpg)

2、**按下图所示效果，参照注释提示信息，完成代码填充。**

<html>

 <head>

 <title> 列表的属性 </title>

 </head>

 <body>

  **<!****— 填充说明：（1）直接使用标记使“最新上榜”标题加粗；（2）指定列表项编号为数字；（3）从第2个开始编号；（4）指定列表项编号为英文大写字母； -->**

​    （1）  

​    <ol  （2）   （3） > 

​    <li>周大侠</li>

​    <li>七月</li>

​    <li  （4）   （5） >是非题</li> 

​    <li>天亮了</li>

​    <li>顺其自然</li>

  </ol>

 </body>

</html>

![image](/Users/xiongshou/markdown/课程/clip_image061.jpg)

 参考答案

![IMG_258](/Users/xiongshou/markdown/课程/clip_image063.jpg)

3、**根据注释提示信息补全代码。**

<html>

 <head> 

  <script type="text/javascript">

   function checkusername(){

​    var Yourname=myform.username.value; 

 if ( （1）  )                //Yourname为空字符或不输入时

 { alert("用户名不能空！");}

 else  

  { var firstchar=Yourname. （2） ; //获取用户输入的首字符

   if (firstchar>="0" && firstchar<="9")  //首字符不能为数字

​    {  alert("用户名第一个字符不能为数字！");

​    }

else {

   if ( （3） )              //Yourname的长度小于6或大于16

​    { alert("用户名长度大于等于6且小于等于16！"); }}}}

  </script>

 </head>

 <body> 

   <form name="myform" method="post" action="">

​    <b>表单验证</b><br> 

用户名：<input type="text" name="username" ><br>

<input type="button" value="检查"  （4） > /*单击并调用函数checkusername */

<input type="reset" value="重置"><br>

   </form>

 </body>

</html>

参考答案

（1）Yourname==”” || Yourname==nul
 （2）charAt(0
 （3）Yourname.length<6 || Yourname.length>16
 （4）onclick=”checkusername();”

4、**按下图所示效果，参照注释提示信息，完成代码填充。**

<html>

 <head>

 <title> 样式表-排版 </title>

  <style type="text/css">

​    .p3{text-transform:capitalize;}

**/\*****类选择p4定义说明：(1)段首空2个字符；(2)设置行高为35px；(3)设置背景色为#000033；(4)设置文字居中对齐(5)设置字符间距为2px;(6)引用样式p4 \*/**

  .p4{   （1）  ;  （2）  ;  （3）  ;  （4）  ; （5） ;  color:#ffffff;}

  </style>

 </head>

<body>

    <p   （6）   >核心提示：3月30日，京东商城推出火车票预订和代购业务。目前提供火车票代购业务的商业网站还有去哪儿网、携程、铁友旅行网（以下简称铁友网）等。铁道部称，12306网站是销售火车票的唯一专业网站，铁路部门没有授权或委托任何其他网站开展火车票发售或代购业务。

  <span class="p3">commissioner, independent commission</span></p>

</body>

</html>

![image](/Users/xiongshou/markdown/课程/clip_image064.jpg)

参考答案

（1）text-indent:2em
 （2）line-height:35px
 （3）background:#000033或background-color: #000033
 （4） text-align:center
 （5）letter-spacing:2px
 （6）class=”p4”

5、**用CSS+DIV完成下图页面布局设计，并按注释提示信息填充代码。**

<!DOCTYPE html>

<html>

 <head>

 <title> DIV+CSS应用 </title>

  <style type="text/css">

\#header{

 （1） ;    **/\*** **头部宽度为100% \*/**

height:70px;background:#99cc66;border-bottom:2px solid #ffffff;}

​    \#mainbody{width:100%;height:200px;border-bottom:2px solid #ffffff;}

​    \#left{

 （2） ;    **/\*****左边盒子向左浮动 \*/**

background:#99cc33;width:20%;height:200px;

 （3） ;    **/\*****盒子右边框2px、实线、白色#ffffff\*/**

}

​    \#middle{

 （4）  ;   **/\*****中间盒子上、下边距为0，左、右边距为25% \*/**

background:#cccc66;height:200px;}

​    \#right{float:right;background:#99cc00;width:20%;height:200px;}

​    \#footer{width:100%;height:50px;background:#995500;}

​    \#clearfloat{clear:both;border-bottom:2px solid #ffcc00;}

 </style>

 </head>

 <body>

     <div   （5）  >头部</div>   /*引用头部样式*/

   <div id="mainbody" >

 <div id="left" >左边</div>

 <div id="right" >右边</div>

 <div id="middle" >中间</div>             

   </div>

<div id="footer" > 页脚</div>

  </body>

</html>

![image](/Users/xiongshou/markdown/课程/clip_image066.jpg)

参考答案

（1）width:100%
 （2）float:left
 （3）border-right:2px solid #ffffff
 （4）margin:0 25%
 （5）id=”header”

6、有一a元素，其结构为<a href=”#”><b>首页</b></a>,它的CSS样式如下，请在下划线处填写代码注释。

a{

font-size:14px;

text-decoration:none;    /*___(1)__*/

background-image:url(pic1.gif);

height:30px;

padding-left:5px;

display:block;       /*___(2)__*/

float:left;         /*___(3)__*/

line-height:30px;    /*___(4)__*/

}

b{

  background-image:url(pic2.gif);

background-position:right top;   /*___(5)__*/

display:block;

width:60px;

}

参考答案

（1）清除超链接的下划线
 （2）将a标记以块级元素显示
 （3）让a标记左浮动
 （4）行高30px
 （5）背景图片定位为右上角开始显示

7、请阅读下面的程序，根据注释中的要求填写代码。

<!DOCTYPE html >

<html >

<head>

<title>超链接标记</title>

</head>

<body>

<a href="#" _____（1）____>  <!--指定链接页面的打开方式为在新窗口中打开-->

<img src="1.jpg" width="200" height="200" _____（2）_____/>  <!--去掉链接图像的边框-->

</a>

</body>

</html>

参考答案

（1）target=”_blank”
 （2）border=”0”

8、在浏览器中运行下面的代码，将会出现的结果为（  ）。

<script type="text/javascript">

var num1=1;

var num2=2;

if(num1<num2){

alert('成立')

}

else{

alert('不成立')

}

alert('ok')

</script> 

参考答案

弹出“成立”对话框，点击“确定”按钮后，弹出“ok”对话框

9、阅读以下代码，并根据要求补全代码。

<body   （1）  ="document.body.style.backgroundColor='blue'"

   （2） ="document.body.style.backgroundColor='red'"

​    （3） ="document.body.style.backgroundColor='#fff'">

   <h3>在页面任意位置按下鼠标背景变蓝色，抬起鼠标变红色，双击鼠标变白色</h3>

</body>

参考答案

（1）onmousedown
 （2）onmouseup
 （3） ondblclick

10、填充说明：（1）外边距属性；（2）边框属性；（3）线型为虚线；（4）input类型为文本；（5）文本域为5行。

 <html>

 <head>

   <title> 表单应用</title>

  <style type=" text/css ">

   fieldset {

​     padding:10px;

​     ___(1)__:10px;

​     width:270px;

​     color:#333;

​    __(2)___:#06c __(3)__1px;

  }

  legend {

​    color:#06c;

   font-weight:800;

​    background:#fff;

   }

  </style>

  </head>

  <body>

 <form name="" method="post" action="">

 <fieldset>

 <legend>个人信息：</legend>

  输入姓名：<input type="__(4)__" name="" size="8" maxlength="12"><br>

  输入爱好：<textarea name="" ___(5)__ cols="20" wrap="">请在此输入信息</textarea><br>

​    </fieldset>

  </form>

  </body>

</html>

![image](/Users/xiongshou/markdown/课程/clip_image068.jpg)

参考答案

（1） margin
 （2） border
 （3） dashed
 （4） text
 （5） rows=”5”