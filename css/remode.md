## 知识点回顾
#### 1.如何在html中使用css
* 在标签内style属性中定义css，例如：\<h1 style="backgroud-color:black">标题\<h1/>
* 在head标签内添加style标签，然后在style中定义css
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
* 引用css文件
```
<head>
    <meta charset="UTF-8">
    <title>work</title>
    <link rel="stylesheet" type="text/css" href="work.css">
</head>
```
#### 