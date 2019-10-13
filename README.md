
# html+css3

​		经过一个月的专项练习，内容包括网站切图，表格表单、html5新特性，ie浏览器的兼容、css3新特性，2d、3d动画，手机端布局（弹性布局），对html+css3的理解和应用更上一个高度。

​		

****

### 下面简单介绍一下重要的知识点：

> 表格： 

~~~html
```
< table>
	<tr>行
		< td>列</td>
        < td>列</td>
	</tr>
< table>
```
~~~
* 属性
  * cellpadding 	盒子与内容的间距
  * colspan 		  合并列 （横向扩展）
  * rowspan 		合并行（竖直向下）

> 表单 form：

```html
<form name=" 表单名称"  method="post/get"  action="#地址" >
文本框
<input type="text" value="默认值" placeholder=“输入框内容/>
密码框
<input type="password" />	
提交按钮
<input type="submit" value="按钮内容" />	
重置按钮
<input type="reset" value="按钮内容" />			
单选框/单选按钮
男<input type="radio" name="ral"/>女<input type="radio" name="ral" />
 <!--单选按钮里的name属性必须写，同一组单选按钮的name属性值必须一样。-->
复选框    
<input type="checkbox" name="like" /><input type="checkbox" name="like"  disabled="disabled" /> (disabled="disabled" :禁用)(checked="checked" :默认选中)
下拉菜单   
<select name=""><option>菜单内容</option></select>				
多行文本框（文本域）    
<textarea name="textareal" cols="字符宽度" rows="行数"></textarea>  禁止拖动 resize: none;
按钮    
<input name="'" type="button" value=“按钮内容” />					
<!--（他和submit的区别是 ，submit是提交按钮 起到提交信息的作用，button只起到跳转的作用，不进行提交。）占位placeholder=“输入框内容” -->

```

>  表单的高级属性

* **fieldset** 表单字段集 作用：给表单控件分组
* **legend表单标题**
* **label提示信息标签**
  写法：

```html
<label for="绑定控件id名"></label><input id="名" type="text">
```

* **上传文件框**：
  &LT;input type=&QUOT;file&QUOT; multiple=&QUOT;multiple&QUOT; /&GT;

* **图像域**：

&LT;input type=&QUOT;image&QUOT; src=&QUOT;&QUOT; width=&QUOT;&QUOT; height=&QUOT;&QUOT;  alt=&QUOT;图片&QUOT; /&GT;



## html5新特性

**兼容到ie9**

增加了新特性：语义特性，本地存储特性，设备兼容特性，连接特性，网页多媒体特性，三维、图形及特效特性，性能与集成特性，CSS3特性。

1.**header**
     定义文档的页眉，通常是一些引导和导航信息
     注意：header不能被header、footer嵌套，header不局限于写在网页头部，也可以写在网页内容里面

2.**nav**
    导航标签
3.**main**
主要内容标签不能出现一个以上的&LT;main> 元素。&LT;main> 元素不能是以下元素的后代：&LT;article>、&LT;aside>、&LT;footer>、&LT;header> 或&LT;nav>


 4.**article**
    比section具有更明确的语义，它代表一个独立的、完整的相关内容块，可独立于页面其它内容使用
    注意：article可以嵌套article
    
5.**section** 
     标签定义了文档的章节，本意是区块 
 6.**aside**
     用来装载非正文的内容，标签被删除不影响页面信息传递，例如：广告、侧边栏 

7.**footer** 
     眉脚一般会包含作者姓名、文档版权信息、使用条款链接、联系信息等. 也可以写在网页内容里面
 8.**hgroup** 
     用于对网页或区段（section）的标题进行组合 

9.**figure、figcaption** 

* &LT;figure>用于对元素进行组合。一般用于图片，文字组合。
* &LT;figcaption>是 figure的子元素，用于对figure的内容进行说明

 ```html
     <figure>
            <img src="../images/mn.jpg" alt="">
            <figcaption>超人气女团</figcaption>
     </figure> 
 ```
10. time标签  datetime属性
    
     <p>今天<time>星期三</time>，好开心，还有三天就<time datetime="2019-7-28">放假</time> 了</p> 
    
11.  datalist 输入功能下拉列表

```html
 <input type="text" list="cn-list">
    <datalist id="cn-list">
        <option value="李宇春">李宇春</option>
        <option value="周笔畅">周笔畅</option>
        <option value="张靓颖">张靓颖</option>
    </datalist>
```

12. details 用于描述文档或文档某个部分的细节  open属性 
 <details open>
        <summary>静夜思</summary>
        <p>锄禾日当午，旱地和下土</p>
        <p>夜来风雨声，花落知多少</p>
 </details>
```  html
    <details open>
        <summary>静夜思</summary>
        <p>锄禾日当午，旱地和下土</p>
        <p>夜来风雨声，花落知多少</p>
    </details>
```
13. mark 定义带有记号的文本
    <p>
        报告显示，2019年中国十大拥堵城市分别是<mark
            style="background:#0f0;">重庆市、哈尔滨市、北京市、长春市、呼和浩特市、大连市、济南市、沈阳市、兰州市、西宁市</mark>。其中，重庆市高峰行程延时指数为1.964，排名十大堵城之首
    </p>

```html
    <p>
        报告显示，2019年中国十大拥堵城市分别是<mark
            style="background:#0f0;">重庆市、哈尔滨市、北京市、长春市、呼和浩特市、大连市、济南市、沈阳市、兰州市、西宁市</mark>。其中，重庆市高峰行程延时指数为1.964，排名十大堵城之首
    </p>
```



14.progress 进度条 max最大值  value当前值
    <progress max="100" value="50"></progress>

```html
   <progress max="100" value="50"></progress>
```



15.meter 度量尺
    <meter max="100" value="50"></meter>

```html
    <meter max="100" value="50"></meter>
```



16.ruby注释标签 配合rt
    <ruby>嫑<rt>biáo</rt></ruby>

```html
<ruby>嫑<rt>biáo</rt></ruby>
```



17.output

<form oninput="res.value=no1.value-no2.value">
        <!-- 加号在js里是字符串拼接 -->
        <input type="text" name="no1" placeholder="请输入数字1">
        <input type="text" name="no2" placeholder="请输入数字2">
        <output name="res"></output>
</form>

```html
<form oninput="res.value=no1.value-no2.value">
        <!-- 加号在js里是字符串拼接 -->
        <input type="text" name="no1">
        <input type="text" name="no2">
        <output name="res"></output>
</form>
```
    18.语义化标签兼容IE8-6
    <!-- 通过<script src="路径"></script>引入外部插件 -->

  






 视频的插入   
```html
<video src="movie.ogg"></video> 
<video Controls ><source src="movie.ogg" type="video/ogg" ></video>
(type必加属性) 支持的视频格式ogg、webM、MP4
```
