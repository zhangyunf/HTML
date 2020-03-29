# JS的三大分类
> 核心(ECMAScript): 描述了该语言的语法和基本对象
> 文档对象模型(DOM)：描述处理网页内容的方法和接口
> 浏览器对象模型(BOM): 描述与浏览器进行交互的方法和接口
# 核心（ECMAScript）
## 1.输出
* 1.1 console.log()
* 1.2 window.alert()
* 1.3 document.write()
* 1.4 innerHTML()
## 2.数据类型
* 2.1 字符串
* 2.2 数字
* 2.3 数组
* 2.4 日期
## 3.
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


