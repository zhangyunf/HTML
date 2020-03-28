## 知识点回顾
#### 1、如何在html中使用css
* 内联式：在标签内style属性中定义css，例如：\<h1 style="backgroud-color:black">标题\<h1/>
* 嵌入式：在head标签内添加style标签，然后在style中定义css
```
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .hide{
            display: none;
        }
        .item .header{
            height: 35px;
            background-color: blue;
            color: white;
            line-height: 35px;
        }
    </style>
</head>
```
* 外联式：引用css文件
```
<head>
    <meta charset="UTF-8">
    <title>work</title>
    <link rel="stylesheet" type="text/css" href="work.css">
</head>
```
#### 2、css基本语法
```
选择器{
属性：值
}
```
## 知识点回顾
#### 1、如何在html中使用css
* 内联式：在标签内style属性中定义css，例如：\<h1 style="backgroud-color:black">标题\<h1/>
* 嵌入式：在head标签内添加style标签，然后在style中定义css
```
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .hide{
            display: none;
        }
        .item .header{
            height: 35px;
            background-color: blue;
            color: white;
            line-height: 35px;
        }
    </style>
</head>
```
* 外联式：引用css文件
```
<head>
    <meta charset="UTF-8">
    <title>work</title>
    <link rel="stylesheet" type="text/css" href="work.css">
</head>
```
#### 2、css基本语法
```
选择器{
属性：值;
}
```
#### 3、选择器
* 3.1 基本选择器
* 3.1.1 通用选择器(*)
```
* {
属性：值;
属性: 值;
}
```
* 3.1.2 标签选择器(标签名)
> 一旦使用标签选择器,则当前页面上的所有该标签全部都有该样式
```
div {
属性：值;
属性: 值;
}
```
* 3.1.3 类选择器(class):标签的class属性值
> 格式: .类名{}
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .className {
            background-color: #903d3d;
        }
    </style>
</head>
<body>
    <div class="className">hello world</div>
</body>
```
* 3.1.4 id选择器
> 格式：#ID名{}
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #IDName {
            color: #903d3d;
        }
    </style>
</head>
<body>
    <div id="IDName">hello world</div>
```
* 3.2 层级选择器
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #IDName #h1 {
            color: #903d3d;
        }
    </style>
</head>
<body>
    <div id="IDName">
        <div id="h2">hello world h2</div>
        <div id="h1">hello world h1</div>
    </div>
</body>
```
* 3.3 组合选择器(逗号隔开)
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #h2,#h1 {
            color: #903d3d;
        }
    </style>
</head>
<body>
    <div id="IDName">
        <div id="h2">hello world h2</div>
        <div id="h1">hello world h1</div>
    </div>
</body>
```
* 3.4 属性选择器（不常用）
>格式:*[属性1][属性2]  两个属性是且的关系
* 3.5 伪类：有条件的选择器

属性|描述
---|---
:active|向被激活的元素添加样式
:focus|向拥有键盘输入焦点的元素添加样式
:hover|当鼠标悬浮在元素上方时，向元素添加样式
:link|向未被访问的链接添加样式
:visited|向已被访问的链接添加样式
:first-child|向元素的第一个子元素添加样式
:lang|向带有指定 lang 属性的元素添加样式
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #h2:hover {
            color: #903d3d;
        }
    </style>
</head>
<body>
    <div id="IDName">
        <div id="h2">hello world h2</div>
        <div id="h1">hello world h1</div>
    </div>
```
* 3.6 伪元素：只能用于块级元素，作用于文本

属性|描述
---|---
:first-letter|向文本的第一个字母添加特殊样式
:first-line|向文本的首行添加特殊样式
:before|在元素之前添加内容
:after|在元素之后添加内容
#### 4、样式
分类|属性|描述|值
---|---|---|---
背景|background|简写属性，作用是将背景属性设置在一个声明中|url(图片) color
|  |background-color|设置元素的背景颜色|--
|  |background-image|把图像设置为背景| url(图片路径)
|  |background-position|设置图像的起始位置|center top bottom right left
|  |background-repeat|设置图像的重复方式|no-repeat(不允许平铺)
|  |background-attachment|背景图像是否随页面滚动|scroll-默认值。背景图像会随着页面其余部分的滚动而移动 fixed-当页面的其余部分滚动时，背景图像不会移动 inherit-规定应该从父元素继承 background-attachment 属性的设置
文本|color|设置文本颜色
|  |direction|设置文本方向
|  |line-height|设置行高
|  |letter-spacing|设置字符间距
|  |text-align|对齐元素中的文本
|  |text-decoration|向文本添加修饰
|  |text-indent|缩进元素中文本的首行
|  |text-shadow|设置文本阴影。CSS2 包含该属性，但是 CSS2.1 没有保留该属性。
|  |text-transform|控制元素中的字母
|  |unicode-bidi|设置文本方向
|  |white-space|设置元素中空白的处理方式
|  |word-spacing|设置字间距
字体|font|简写属性
|  |font-size|字体大小
|  |font-style|字体风格|normal-正常显示 italic-斜体 oblique-倾斜
|  |font-weight|字体粗细
链接|text-decoration|去掉下划线|none-无下划线 underline-有下划线
列表|list-style|简写属性。用于把所有用于列表的属性设置于一个声明中。
|  |list-style-image|将图象设置为列表项标志|url(图片地址)
|  |list-style-position|设置列表中列表项标志的位置|inside-列表项目标记放置在文本以内，且环绕文本根据标记对齐  outside-默认值。保持标记位于文本的左侧。列表项目标记放置在文本以外，且环绕文本不根据标记对齐
|  |list-style-type|设置列表项标志的类型|none-无标记 disc-默认实心圆 circle-空心圆 square-实心方块 其它-[参考地址](https://www.w3school.com.cn/cssref/pr_list-style-type.asp)
表格|border-collapse|设置是否把表格边框合并为单一的边框。|separate-默认值。边框会被分开。不会忽略 border-spacing 和 empty-cells 属性。 collapse-如果可能，边框会合并为一个单一的边框。会忽略 border-spacing 和 empty-cells 属性。
|  |border-spacing|设置分隔单元格边框的距离。
|  |caption-side|设置表格标题的位置| top-顶部 bottom-底部
|  |empty-cells|设置是否显示表格中的空单元格|hide-不在空单元格周围绘制边框。 show-在空单元格周围绘制边框。默认。
|  |table-layout|设置显示单元、行和列的算法。
轮廓|outline|在一个声明中设置所有的轮廓属性
|  |outline-color|设置轮廓的颜色
|  |outline-style|设置轮廓的样式|[参考地址](https://www.w3school.com.cn/cssref/pr_outline-style.asp)
|  |outline-width|设置轮廓的宽度
框模型|border|边框|宽度-border-width 样式- border-style[参考地址](https://www.w3school.com.cn/cssref/pr_border-style.asp)  颜色- border-color
|    |margin|外边距|auto-规定的是均等地分配可用的外边距。结果就是居中的元素
|    |padding|内边距|
定位|position|把元素放置到一个静态的、相对的、绝对的、或固定的位置中|absolute-绝对，相对于 static 定位以外的第一个父元素进行定位 fixed-绝对，相对于浏览器窗口进行定位<br/>  relative-生成相对定位的元素，相对于其正常位置进行定位 static-默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）
|  |top|定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。
|  |right|定义了定位元素右外边距边界与其包含块右边界之间的偏移。
|  |bottom|定义了定位元素下外边距边界与其包含块下边界之间的偏移。
|  |left|定义了定位元素左外边距边界与其包含块左边界之间的偏移。
|  |overflow|设置当元素的内容溢出其区域时发生的事情|[参考地址](https://www.w3school.com.cn/cssref/pr_pos_overflow.asp)
|  |clip|设置元素的形状。元素被剪入这个形状之中，然后显示出来。
|  |vertical-align|设置元素的垂直对齐方式。
|  |z-index|设置元素的堆叠顺序。
其它|opacity|透明度
分类属性|clear|设置一个元素的侧面是否允许其他的浮动元素。
|     |cursor|规定当指向某元素之上时显示的指针类型。
|     |display|设置是否及如何显示元素|block-此元素将显示为块级元素，此元素前后会带有换行符。 inline-默认。此元素会被显示为内联元素，元素前后没有换行符。 inline-block-行内块元素
|     |float|定义元素在哪个方向浮动
|     |position|把元素放置到一个静态的、相对的、绝对的、或固定的位置中。
|     |visibility|设置元素是否可见或不可见