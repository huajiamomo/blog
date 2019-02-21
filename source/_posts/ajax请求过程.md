---
title: ajax请求过程
date: 2018-07-13 18:26:12
tags:
---

### 1.创建Ajax核心对象
var oAjax=new XMLHttpRequest();
注意：处理兼容问题  if(window.XMLHttpRequest){}else{}
<!-- more -->

### 2.向服务器发送请求
a.get请求
    oAjax.open('GET','url',true);
    oAjax.send();
b.post请求
    oAjax.open('POST','url',true);
    oAjax.setRequestHeader('content-type','');//设置请求头
    oAjax.send('string参数');
注意：true异步请求  false同步请求

### 3.服务器响应，接收数据
oAjax.onreadystatechange=function(){};
a.请求状态 oAjax.readyState
    0：请求未初始化
    1：服务器连接建立
    2：请求已接收
    3：请求处理中
    4：请求处理完成，响应已就绪  在这个时候获得数据
b.响应状态码 oAjax.status
    200：成功
    304：该资源在上次请求后没有任何修改（浏览器的缓存机制）
    403：服务器拒绝请求
    404：服务器找不到请求的网页
    408：请求超时
    500：服务器内部错误