---
title: HTTP入门
tags: HTTP
grammar_cjkRuby: true
categories: web前端
---


## HTTP简介
超文本传输协议（HyperText Transfer Protocol，缩写：HTTP）是一种用于分布式、协作式和超媒体信息系统的应用层协议。HTTP是万维网的数据通信的基础。设计HTTP最初的目的是为了提供一种发布和接收HTML页面的方法。通过HTTP或者HTTPS协议请求的资源由统一资源标识符（Uniform Resource Identifiers，URI）来标识。
## URN、URL、URI

- URL：统一资源定位符
- URI：统一资源标识符

通常来说，URL就是是使用浏览器等访问web页面的时候需要输入的网页地址，列如：
``` stylus
www.google.com
```
URL组成： ==协议、域名、端口号、路径、查询字符串、锚点==
### URI
是更通用的资源标识符，URI由两个主要的子集构成

1. URL：通过描述资源的位置来描述资源
2. URN：通过名字来识别资源，和位置无关
 
 URI 是 Uniform Resource Identifier 的缩写
 
- Uniform：规定统一的格式，可方便处理各种不同类型的资源，而不用根据上下文环境来识别资源指定的访问方式，加入新的协议方案(HTTP, HTTPS, FTP等)也更容易
- Resource：资源的定义是“可以标识的任何东西”，除了文档文件、图像或者服务（天气预报）等能够区别于其他类型的，劝都可以称为资源，另外资源不仅可以是单一的，也可以是多数的集合体

- Identifier：表示可标识的对象，也成为标识符

综上所述，URI就是某个协议方案表示的资源的定位标识符，协议方案是指访问资源所使用的协议类型名称，采用HTTP协议的时候，协议方案就是http，除此之外还有ftp、mailto、file等。
## DNS
域名系统（Domain Name System，缩写：DNS）是互联网的一项服务。它作为将域名和IP地址相互映射的一个分布式数据库，能够使人更方便地访问互联网。
## 请求与响应
- 浏览器负责发起请求
- 服务器在 80 端口接收请求
- 服务器负责返回内容（响应）
- 浏览器负责下载响应内容

HTTP 的作用就是指导浏览器和服务器如何进行沟通。（Server + Client + HTTP）
### 请求格式

``` stylus
1 动词 路径 协议/版本
2 Key1: value1
2 Key2: value2
2 Key3: value3
2 Content-Type: application/x-www-form-urlencoded
2 Host: www.baidu.com
2 User-Agent: curl/7.54.0
3 
4 要上传的数据
```
1. 请求最多包含四部分，最少包含三部分。（也就是说第四部分可以为空）
2. 第三部分永远都是一个回车（\n）
3. 动词有 GET POST PUT PATCH DELETE HEAD OPTIONS 等
4. 这里的路径包括「查询参数」，但不包括「锚点」
5. 如果你没有写路径，那么路径默认为 /
6. 第 2 部分中的 Content-Type 标注了第 4 部分的格式

### 请求实列
请求内容

``` stylus
POST / HTTP/1.1
Host: www.baidu.com
User-Agent: curl/7.54.0
Accept: */*
Frank: xxx
Content-Length: 10
Content-Type: application/x-www-form-urlencoded

1234567890
```
请求内容

``` stylus
GET / HTTP/1.1
Host: www.baidu.com
User-Agent: curl/7.54.0
Accept: */*
Frank: xxx
```
### 响应格式

请求了之后，应该都能得到一个响应，除非断网了，或者服务器宕机了。

``` stylus
1 协议/版本号 状态码 状态解释
2 Key1: value1
2 Key2: value2
2 Content-Length: 17931
2 Content-Type: text/html
3
4 要下载的内容
```

1. 状态码
   - 1xx消息——请求已被服务器接收，继续处理
   - 2xx成功——请求已成功被服务器接收、理解、并接受
   - 3xx重定向——需要后续操作才能完成这一请求
   - 4xx请求错误——请求含有词法错误或者无法被执行
   - 5xx服务器错误——服务器在处理某个正确请求时发生错误
2. 状态解释
3. 第 2 部分中的 Content-Type 标注了第 4 部分的格式
4. 第 2 部分中的 Content-Type 遵循 MIME 规范

### 响应实列
响应内容

``` stylus
HTTP/1.1 302 Found
Connection: Keep-Alive
Content-Length: 17931
Content-Type: text/html
Date: Tue, 10 Oct 2017 09:19:47 GMT
Etag: "54d9749e-460b"
Server: bfe/1.0.8.18

<html>
<head>
<meta http-equiv="content-type" content="text/html;charset=utf-8">
......代码太多，省略
```


