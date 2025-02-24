## 1.html格式

#### 1.语法规范

##### 1.1基本语法概述

1.HTML标签是由尖括号构成的关键词；

2.通常成对出现，例如<html>和</html>，这称为双标签；

3.极少情况下有单标签，例如<br />

##### 1.2标签关系

包含关系和并列关系

#### 2.基本结构标签

##### 2.1第一个HTML网页

```html
<html>
   <head>
       <title>我的第一个页面标签</title>
   </head>
   <body>
       加油
   </body>
</html>
```



#### 3.开发工具

##### 3.1 文档类型声明标签

```html
<!DOCTYPE html>
```

文档类型声明，作用就是告诉浏览器使用哪种HTML版本来显示网页；必须写在整个代码最开始

##### 3.2 lang语言种类

```html
<html lang="zh-CN"
```

用来定义当前文档显示的语言（其实都能显示）

1.en定义语言为英语

2.zh-CN定义语言为中文

##### 3.3 字符集

便于计算机识别和存储各种文字

```html
<head>
   <meta charset="UTF-8"/>
</head>
```

#### 4.VS code快捷键

1.快速复制一行：shift+Alt+下箭头（上箭头） 

2.选定多个相同的单词：ctrl+d

3.添加多个光标：ctrl+Alt+上箭头（下箭头）

4.全局替换某些单词：ctrl+h

5.快速定位到某一行：ctrl+g

6.选择某个区块：shift+Alt 然后拖动鼠标

7.放大缩小整个编辑器界面：ctrl++/ctrl+-

8.可以自定义快捷键

#### 5.HTML常用标签

##### 5.1 标签语义

就是标签的含义，在合适的地方加上合适的标签

##### 5.2 标题标签

```html
<body>
   <h1>我是一级标题</h1>
   <h6>我是六级标题</h6>
</body>
```

##### 5.3 段落和换行标签

###### 1.段落标签

```html
<p>我是一个段落标签</p>
```

###### 2.换行标签

```html
<br />
```

##### 5.4 文本格式化标签

为文字设置粗体，下划线，斜体等效果，需要用到HTML中的文本格式化标签；

```html
<strong>加粗标签</strong>   <b></b>
<em>倾斜标签</em>           <i></i>
<del>删除线</del>           <s></s>
<ins>下划线</ins>           <u></u>
```

##### 5.5 盒子标签

```html
<div>这是头部</div> 一行只能放一个
<span>跨步 跨距</span> 一行好多个
```

##### 5.6 图像标签和路径

###### 1.图像标签

```html
<img src="图像URL" />    必须属性，它用于指定图像文件的路径和文件名
<img alt="文本" />       替换文本，图像不能显示的文字
<img title="文本" />     提示文本，鼠标放到图像上显示的文字
<img width="像素" />     设置图像的宽度
<img heigth="像素" />    设置图像的高度 和宽度二选一避免失真
<img border="像素" />    设置图像的边框粗细
```

注意点：

图像标签可以拥有多个属性，必须写在标签名后边；

属性之间不分先后顺序，标签名与属性、属性与属性之间均以空格分开；

属性采取键值对的格式，即key="value"的格式，属性=“属性值”。

###### 2.路径

目录文件夹，根目录（打开目录文件夹的第一层）

相对路径：（图片相对于HTML文件的位置）

同一级路径

```html
<img src="baidu.gif"/>
```

下一级路径

```html
<img src="images/baidu.gif"/>  引用images文件夹中的baidu.gif文件
```

上一级路径

```html
<img src="../baidu.gif"/>   上几级就加几个../
```

绝对路径：

在目录中的绝对位置，通常是由电脑盘符开始；

```html
<img src="E:\张岐奕1\EPI\github\html"/>  只能在自己的电脑用
<img src="https://renrys.com/revodplay/78871-1-1.html"/>
```

##### 5.7 超链接标签

###### 1.链接的语法格式

```html
<a href="跳转目标"target="目标窗口的弹出方式">文本或图像</a>
```

href：用于指定链接目标的url地址（必须属性）

target：用于指定链接页面的打开方式；

_self为默认值，即当前页面直接显示

_blank为在新窗口中的打开方式

###### 2.链接的分类

外部链接：格式要求，写该网站地址

```html
<a href="http://www.qq.com" target="_self">腾讯</a>
<a href="http://www.qq.com" target="_blank">腾讯</a>
```

内部链接：自己的文件夹中有该文件，直接写该文件名称

```html
<a href="输入文件名称" target="_blank">文件名称</a>
```

空链接：

```html
<a href="#">这是个空链接</a>
```

下载链接：如果href里面地址是一个文件或者压缩包，会下载这个文件

```html
<a href="返校.zip"/>下载文件</a>
```

网页元素链接：在网页中的各种网页元素如文本 图像 表格 音频 视频等都能添加超链接

```html
<a href="http://www.baidu.com"><img src="返校.jpg"/>点开即百度网页</a>
```

锚点链接：点击链接可以快速定位到页面中的某个位置

```html
<a href="#任意名字">个人经历</a>
在任意一个标签中输入id=“相同名字”即可
例如
<a href="#123">个人经历</a>
<h4 id="123">个人经历介绍</h4>
此时，点击第一个个人经历就能迅速定位到下方的个人经历介绍；
```

#### 6.HTML中的注释和特殊字符

##### 6.1 注释（不执行也不显示到页面中）

快捷键：ctrl+/

```html
<!--我是Camellia-->
```

##### 6.2 特殊字符

一个&是一个特殊字符

```html
     空格符              &nbsp;
<    小于号              &lt;
>    大于号              &gt;
&    和号                &amp;
￥   人民币               &yen;
©    版权                &copy;
     注册商标             &reg;
°    摄氏度              &deg;
±    正负号              &plusmn;
✖    乘号               &times;
➗   除号               &divide;
²    平方（上标2）        &sup2;
³    立方（上标3）        &sup3;
```

#### 7.HTML标签

##### 7.1 表格标签

###### 1.表格的主要作用

不是用来布局页面的，是用来展示数据的；

###### 2.表格的基本语法

```html
<table>                                          用于定义表格的标签
   <tr>                                          用于定义表格中的行
      <td>单元格里的文字</td>                       表格中的单元格
   ...
   </tr>
   ...
</table>
```

###### 3.表头单元格标签

```html
<table>
   <tr>
      <th> 居中且加粗</th>
   </tr>
</table>
```

###### 4.表格属性

```html
属性名         属性值                  描述
align         left,right,center      规定表格相对周围元素的对齐方式
border        1或""                  规定表格单元是否有边框，默认""没有边框
cellpadding   像素值                  规定单元边沿与其内容之间的空白，默认1像素
cellspacing   像素值                  规定单元格之间的空白，默认为2像素(线宽)
width         像素值或百分比           规定表格的宽度
```

```html
<table align="laft"></table>
```

###### 5.表格结构标签

把表格划分为表格头部和表格主体两部分；

```html
<table>
   <thead>                  内部必须有tr标签
      <tr>
         <th>...</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>...</td>
      </tr>
   </tbody>
</table>
```

###### 6.合并单元格

方式：

1.跨行合并：rowspan=“合并单元格的个数”

2.跨列合并：colspan="合并单元格的个数"

目标单元格：（写合并代码）

1.跨行：最上侧单元格为目标单元格，写合并代码；

2.跨列：最左侧单元格为目标单元格，写合并代码；

```html
<td rowspan="2"></td>
```

##### 7.2 列表标签

###### 1.无序列表

ul 标签中只能放 li 标签，li 标签中可以放其他标签

去掉前方小圆点：css

```html
<style>
	li {
	list-style: none;
	}
</style>
```



```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
    ...
</ul>
```

###### 2.有序列表

```html
<ol>
    <li>1</li>
    <li>2</li>
    <li>3</li>
    ...
</ol>
```

###### 3.自定义列表

```html
<dl>
    <dt> 名词1 </dt>
    <dd> 解释1 </dd>
    <dd> 解释2 </dd>
    <dd> 解释3 </dd>
    ...
</dl>
```

##### 7.3表单标签

###### 1.目的

收集用户信息

###### 2.组成

包括表单域，表单控件（表单元素）和提示信息

###### 3.表单域

实现用户信息的收集和传递

form会独占一行，若使其不独占一行，则

```html
<head>
    <style>
        form {
            display:inline-block;
        }
    </style>
</head>
<body>
    <form>
        ...
    </form>
</body>
```



```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

action      url地址          用于指定接收并处理表单数据的服务器程序的url地址

method   get/post        用于设置表单数据的提交方式

name       名称               用于指定表单的名称，以区分同一个页面中的多个表单域

###### 4.表单控件

1.input 输入表单元素

```html
<input type="属性值"/>
```

属性值：

button                  定义可点击按钮（多数情况下，用于通过JavaScript启动脚本）

checkbox             定义复选框

file                         定义输入字段和“浏览”按钮，供文件上传

hidden                  定义隐藏的输入字段

image                   定义图像形式的提交按钮

password             定义密码字段，该字段中的字符被掩码

radio                     定义单选按钮

reset                     定义重置按钮，重置按钮会清除表单中的所有数据

submit                  定义提交按钮，提交按钮会把表单数据发送到服务器

text                        定义单行的输入字段，用户可在其中输入文本，默认宽度为20个字符

```html
<input type="radio" name="1"/>
```

属性

name                   用户自定义                定义input元素的名称

value                   用户自定义                 规定input元素的值

checked              checked                      规定此input元素首次加载时应当被选中

maxlength          正整数                         规定输入字段中字符的最大长度

```html
<input type="text" name="username" value="请输入用户名" checked="checked">
```

name 和value 是每个表单元素都有的属性值,主要给后台人员使用.

name 表单元素的名字, 要求单选按钮和复选框要有相同的name值.

checked属性主要针对于单选按钮和复选框, 主要作用一打开页面,就要可以默认选中某个表单元素.

maxlength是用户可以在表单元素输入的最大字符数, 一般较少使用.

2.label标签

<label>标签用于绑定一个表单元素, 当点击<label> 标签内的文本时，浏览器就会自动将焦点(光标)转到或者选择对应的表单元素上,用来增加用户体验；

```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex"/>
```

核心：<label> 标签的for 属性应当与相关元素的id 属性相同。

3.select表单元素

```html
<select>
    <option>1</option>
    <option>2</option>
    <option>3</option>
    ...
</select>
```

4.textarea表单元素

用户输入内容较多时使用

```html
<textarea cols="6" rows="5">
    内容           
</textarea>
```

