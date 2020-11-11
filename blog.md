# CSS知识总结

本篇将主要介绍和概括一下内容：

- 渲染树（html DOM, CSSOM, render tree）
- 浏览器的渲染原理
- 三种渲染更新方式
- transform实现简单动画
- animation实现简单动画


<br />

<a name="uzKwW"></a>
## 渲染树
<a name="0d7G7"></a>
### 什么是DOM？
DOM的是文件对象模型，英文全称(Document Object Model)。MDN文档描述：“_文档对象模型 (DOM) 是HTML和XML文档的编程接口。它提供了对文档的结构化的表述，并定义了一种方式可以使从程序中对该结构进行访问，从而改变文档的结构，样式和内容。”_<br />_<br />简单来说，DOM模型以逻辑树的形式表达文档，其结构由**节点**和**对象**构成。<br />树的每个分支的终点都是一个节点(node)，每个节点都包含着对象(objects)。<br />例如html分支有两个节点，对象分别是head和body。<br />
<br />![](https://cdn.nlark.com/yuque/0/2020/png/2655081/1604457237440-b1343cb6-a538-4ff8-96ab-e6cc8392f628.png#align=left&display=inline&height=561&margin=%5Bobject%20Object%5D&originHeight=561&originWidth=1199&status=done&style=none&width=1199)<br />上图片以html和css为示例，展示树结构和渲染树。渲染树展视可视节点及其属性，对于不可视节点例如head，meta是不显示的。<br />
<br />
<br />

<a name="GQT1M"></a>
## 浏览器的渲染原理


<a name="LSLVp"></a>
### 浏览器渲染步骤

- 根据html构建html树（DOM）
- 根据css构建css树（CSSOM）
- 两棵树合并成渲染树
- Layout布局 （文档流，盒模型，位置大小等）
- Paint绘制 （显示边框，颜色，阴影等）
- Composite合成 （根据层叠关系显示画面）


<br />![](https://cdn.nlark.com/yuque/0/2020/png/2655081/1604457245170-e5959bd4-f29c-4f14-8df2-b6e31cbc5427.png#align=left&display=inline&height=826&margin=%5Bobject%20Object%5D&originHeight=826&originWidth=1052&status=done&style=none&width=1052)<br />

<a name="OWqXr"></a>
### 如何判断渲染步骤？
以chrome为例，F12打开开发者工具，按esc弹出console “：”<br />选择rendering，flash painting. 每次绿光都是一次渲染

<a name="XPFCr"></a>
## CSS动画的两种做法

1. transition
1. animation


<br />以下直接用实例展示用法：<br />[transition基础实例](http://js.jirengu.com/duwonipozi/2/edit?html,css,js,output)<br />[transition两次](http://js.jirengu.com/gotelihixu/1/edit?html,css,js,output)<br />[animation示例](http://js.jirengu.com/cedoronati/1/edit?html,css,js,output)<br />[hover跳动的心](http://js.jirengu.com/keniberihi/1/edit?html,css,output)<br />[animation跳动的心](http://js.jirengu.com/sepunapahe/1/edit?html,css,output)<br />
<br />_资料来源：饥人谷_

