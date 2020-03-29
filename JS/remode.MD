# JS的三大分类
> 核心(ECMAScript): 描述了该语言的语法和基本对象
> 文档对象模型(DOM)：描述处理网页内容的方法和接口
> 浏览器对象模型(BOM): 描述与浏览器进行交互的方法和接口
# 核心（ECMAScript）
## 1.存在形式
* 1.1 Script代码块只能在当前页面使用
* 1.2 独立js文件，可以引入
```angular2html
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <script type="text/javascript">
        //内部编写JS代码的地方
    </script>
    <!--外部路径引入JS-->
    <script type="text/javascript" src="js路径"></script>

</body>
```
## 2.变量
```angular2html
<script type="text/javascript">
        //全局变量
        na = '张三';
        function func() {
            //局部变量
            var age = 18;
            //全局变量
            a = 20;
        }
    </script>
```
## 2.输出
* 1.1 console.log()
* 1.2 window.alert()
* 1.3 document.write()
* 1.4 innerHTML()
## 3.数据类型
* 2.1 字符串
> 常用方法

方法|描述
---|---
name[0]|索引
length|长度
trim()|去除空白
charAt(index)|根据索引获取字符
subString(start,end)|根据索引获取子序列
split()|分割
```angular2html
<body>
    <div id="d1">HTML标签和样式</div>
    <script>
        setInterval(function () {
            var element = document.getElementById("d1");
            var text = element.innerText;
            var lastText = text.charAt(text.length-1);
            var preString = text.substring(0, text.length - 1);
            element.innerText = lastText + preString;
        }, 1000);
    </script>
</body>
```
* 2.2 数字

方法|描述
---|---
isNaN()|确定某个值是否是个数
infinity()|计算数时超出最大可能数范围时返回的值
Number()|返回数字，由其参数转换而来。
parseFloat()|解析其参数并返回浮点数。
parseInt()|解析其参数并返回整数。

* 2.3 数组
> 初始化
```javascript
var names = ["张三", "李四"];
var names = Array("张三", "李四");
```
>常见方法

方法|描述
---|---
names[0]|索引
push()|尾部追加
pop()|尾部删除
unshift()|头部增加
shift()|头部删除
splice(index, 0, ele)|指定位置插入元素
splice(index, 1, ele)|指定位置替换元素
splice(index, 1)|指定位置删除元素
slice(start, end)|切片
reverse()|翻转
join()|将元素连接起来构建一个字符串
concat()|连接数组
sort()|排序

* 2.4 日期
* 2.5 布尔
```javascript
var status = true;
var status = false;
```
* 2.6 字典
> 声明
```javascript
var info = {
    name: "张三",
    age: 18
}
```
> 常用方法

方法|描述
---|---
info["name"]| 获取
info["age"] = 20|修改
info["sex"] = "女"|增加
delete info["sex"]| 删除
```angular2html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        table {
            border-collapse: collapse;
        }
        table th, table td {
            border: 1px solid #dddddd;
            padding: 8px;
        }
        table th {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div>
        <label>
            <input type="button" onclick="func()" value="添加一个人员"/>
        </label>

    </div>
    <table>
        <thead>
            <tr>
                <th>学号</th>
                <th>姓名</th>
                <th>性别</th>
            </tr>
        </thead>
        <tbody id="body"></tbody>
        <script type="text/javascript">
            var userList = [
                {id:1, name:"张三", sex:"男"},
                {id:2, name:"翠花", sex:"女"},
                {id:3, name:"李四", sex:"男"}
            ]
            count = 0;
            function func() {
                var element = document.getElementById("body");
                if (count < userList.length) {
                    var user = userList[count];
                    var trNode = document.createElement("tr");
                    for (var key in user) {
                        var tdNode = document.createElement("td");
                        tdNode.innerText = user[key];
                        trNode.appendChild(tdNode);
                    }
                    element.appendChild(trNode);
                    count++;
                }else {
                    window.alert("没有人员了");
                }

            }
        </script>

    </table>
</body>
</html>
```
## 
* 1.1 ==和===区别
> '=='只比对值、'==='需要类型和值同时相等
# 文档对象模型(DOM)
## 1.DOM节点
* 1.1 属性

属性|描述
---|---
attributes|节点的属性节点
nodeType|节点类型
nodeName|节点名称
nodeValue|节点值
innerHTML|节点的文本值
parentNode|父节点
firstNode|节点下第一个子元素
lastNode|节点下最后一个子元素
childNodes|节点后的子节点
parentElement|父节点标签内的元素
childElement|所有子节点
firstElementChild|第一个子节点
lastElementChild|最后一个子节点
nextElementSibling|下一个兄弟标签元素
previousElementSibling|上一个兄弟标签
classList|add()-增加
|        |remove()-移除
|        |toggle()-切换
|        |contains()-判断是
|        |contains()-判断是否有对应类名
style|添加css样式

* 1.2 获取标签节点

属性|描述
---|---
document.getElementById()|根据id属性获取节点
document.getElementByTagName()|根据标签名获取节点的数组
documeng.getElementByName()|根据name属性获取符合条件的节点数组
document.getElementsByClassName|根据节点的类名获取标签的伪数组 ，ie8不支持，他是h5标准
document.querySelector("#id名")|获取指定id的标签节点
document.querySelectorAll(".类名")|获取指定选择器的节点

## 2.事件

事件|方法
---|---
用户点击某个对象时调用的事件句柄|onclick()
用户双击某个对象时调用的事件句柄|ondblclick()
元素获取焦点|onfocus()
元素失去焦点|onblur()
域的内容被改变|onchange()
键盘按键被按下|onkeydown()
键盘按键被松开|onkeyup()
页面或图像完成加载|onload()
鼠标按键被按下|onmousedown()
鼠标被移动|onmousemove()
鼠标从某个元素移开|onmouseout()
鼠标移到某个元素之上|onmouseover()
鼠标从元素离开|onmouseleave()
文本被选中|onselect()
确认按钮被点击|onsubmit()
添加class|classListAdd

## 3.增删改

# 浏览器对象模型(BOM)
## 1.window对象

描述|属性
---|---
显示带有一段消息和一个确认按钮警告框|alert()
显示带有一段消息以及确认按钮和取消按钮的对话框,返回状态|confirm()
显示课题是用户输入的对话框,返回输入值|prompt()
打开一个新的浏览器窗口或查找一个已命名的窗口|open()
关闭浏览器|close()
按照指定的周期来调用函数或计算器|setInterval()
把内容滚动到指定的坐标|scrollTo()

## 2.history对象：访问过的URL

描述|属性
---|---
返回浏览器历史里列表中的url数量|length
加载history的前一个url|back()
加载history的下一个url|forward()
加载history的某个具体页面|go()

## 3.location对象

描述|属性
---|---
加载url|location.assign(url)
重新加载|location.reload()
替换当前的url|location.replace(url)


