---
title: flex布局
---


Flex是Flexible Box的缩写，意为”弹性布局”，用来为盒状模型提供最大的灵活性。
采用Flex布局的元素，称为Flex容器（flex container），简称”容器”。它的所有子元素自动成为容器成员，称为Flex项目（flex item），简称”项目”。

### 一、Flex容器：
1.任何一个容器都可以指定为Flex布局。
    .box{display: flex;}
    .box{display: inline-flex;} // 行内元素也可以使用Flex布局
    .box{display: -webkit-flex; /* Safari */display: flex;} // Webkit内核的浏览器，必须加上-webkit前缀。
<!-- more -->
2.容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。
3.容器的属性
    flex-direction
    flex-wrap
    flex-flow
    justify-content
    align-items
    align-content

### 二、Flex项目 
1.项目的属性
    order
    flex-grow
    flex-shrink
    flex-basis
    flex
    align-self
