---
title: Cookie的使用
date: 2018-10-23 13:15:09
tags:
---

Cookie 用于存储 web 页面的用户信息。
cookie 是存储于访问者的计算机中的变量。每当同一台计算机通过浏览器请求某个页面时，就会发送这个 cookie。你可以使用 JavaScript 来创建和取回 cookie 的值。
### 特点：  
1.大小不能超过4K
2.默认不能跨域
3.生存周期，默认是关闭浏览器时清空，可以自己设置过期时间expires
<!-- more -->
### 参数：
1.可以设置cookie的值，过期时间，路径，域
document.cookie="username=John Doe; expires=Thu, 18 Dec 2043 12:00:00 GMT; path=/;domain=domain";
2.关于路径path
默认只有与创建 cookie 的页面在同一个目录或子目录下的网页才可以访问
把 cookie 设置在跟目录下,这样不管是哪个子页面创建的 cookie，所有的页面都可以访问到了:
document.cookie = "name=Darren;path=/"
3.关于域名domain
一定的是同域之间的访问，不能把domain的值设置成非主域的域名。

### 操作：
可以对cookie进行增删改查：创建cookie，删除cookie，修改cookie，获取cookie的值
删除就是把生效时间expires设置为过去的时间

### cookie的安全性：
通常 cookie 信息都是使用HTTP连接传递数据，信息容易被窃取。
假如 cookie 中所传递的内容比较重要，那么就要求使用加密的数据传输。
cookie 的加密属性的名称是“secure”，默认的值为空。如果一个 cookie 的属性为secure，那么它与服务器之间就通过HTTPS或者其它安全协议传递数据。语法如下：
　　document.cookie = "username=Darren;secure"
把cookie设置为secure，只保证 cookie 与服务器之间的数据传输过程加密，而保存在本地的 cookie文件并不加密。如果想让本地cookie也加密，得自己加密数据。