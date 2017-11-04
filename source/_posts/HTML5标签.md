---
title: HTML5标签列表
tags: HTML
categories: web前端
---
## 根元素

``` stylus
Element	Description
<html>	代表 HTML 或 XHTML 文档的根。其他所有元素必须是这个元素的子节点。
```
## 文档元数据

``` stylus
Element	Description
<head>	代表关于文档元数据的一个集合，包括脚本或样式表的链接或内容。
<title>	   定义文档的标题，将显示在浏览器的标题栏或标签页上。该元素只能包含文本，包含的标签不会被解释。
<base>	定义页面上相对 URL 的基准 URL。
<link>	  用于链接外部的 CSS 到该文档。
<meta> 定义其他 HTML 元素无法描述的元数据。
<style>	用于内联 CSS。
```
## 脚本

``` stylus
Element	Description
<script>	定义一个内联脚本或链接到外部脚本。脚本语言是 JavaScript。
<noscript>	定义当浏览器不支持脚本时显示的替代文字。
<template> 这个元素在 HTML5 中加入	通过 JavaScript 在运行时实例化内容的容器。
```
## 章节

``` stylus
Element	Description
<body>	代表 HTML 文档的内容。在文档中只能有一个 <body> 元素。
<section> 这个元素在 HTML5 中加入	定义文档中的一个章节。
<nav> 这个元素在 HTML5 中加入	定义只包含导航链接的章节。
<article> 这个元素在 HTML5 中加入	定义可以独立于内容其余部分的完整独立内容块。
<aside> 这个元素在 HTML5 中加入	定义和页面内容关联度较低的内容——如果被删除，剩下的内容仍然很合理。
<h1>,<h2>,<h3>,<h4>,<h5>,<h6>	标题元素实现了六层文档标题，<h1> 是最大的标题，<h6> 是最小的标题。标题元素简要地描述章节的主题。
<header> 这个元素在 HTML5 中加入	定义页面或章节的头部。它经常包含 logo、页面标题和导航性的目录。
<footer> 这个元素在 HTML5 中加入	定义页面或章节的尾部。它经常包含版权信息、法律信息链接和反馈建议用的地址。
<address>	定义包含联系信息的一个章节。
<main>这个元素在 HTML5 中加入	定义文档中主要或重要的内容。
```
## 组织内容

``` stylus
Element	Description
<p>	    定义一个段落。
<hr>	代表章节、文章或其他长内容中段落之间的分隔符。
<pre>	代表其内容已经预先排版过，格式应当保留 。
<blockquote>	代表引用自其他来源的内容。
<ol>	定义一个有序列表。
<ul>	定义一个无序列表。
<li>	定义列表中的一个列表项。
<dl>	定义一个定义列表（一系列术语和其定义）。
<dt>	代表一个由下一个 <dd> 定义的术语。
<dd>	代表出现在它之前术语的定义。
<figure> 这个元素在 HTML5 中加入	代表一个和文档有关的图例。
<figcaption> 这个元素在 HTML5 中加入	代表一个图例的说明。
<div>	代表一个通用的容器，没有特殊含义。
```
## 文字形式

``` stylus
Element	Description
<p>	    定义一个段落。
<hr>	代表章节、文章或其他长内容中段落之间的分隔符。
<pre>	代表其内容已经预先排版过，格式应当保留 。
<blockquote>	代表引用自其他来源的内容。
<ol>	定义一个有序列表。
<ul>	定义一个无序列表。
<li>	定义列表中的一个列表项。
<dl>	定义一个定义列表（一系列术语和其定义）。
<dt>	代表一个由下一个 <dd> 定义的术语。
<dd>	代表出现在它之前术语的定义。
<figure> 这个元素在 HTML5 中加入	代表一个和文档有关的图例。
<figcaption> 这个元素在 HTML5 中加入	代表一个图例的说明。
<div>	代表一个通用的容器，没有特殊含义。
```
## 编辑

``` stylus
Element	Description
<ins>	定义增加 到文档的内容。
<del>	定义从文档移除 的内容。
```
## 嵌入内容

``` stylus
Element	Description
<img>	代表一张图片 。
<iframe>	代表一个内联的框架 。
<embed> 这个元素在 HTML5 中加入	代表一个嵌入 的外部资源，如应用程序或交互内容。
<object>	代表一个外部资源 ，如图片、HTML 子文档、插件等。
<param>	代表 <object> 元素所指定的插件的参数 。
<video> 这个元素在 HTML5 中加入	代表一段视频 及其视频文件和字幕，并提供了播放视频的用户界面。
<audio> 这个元素在 HTML5 中加入	代表一段声音 ，或音频流 。
<source> 这个元素在 HTML5 中加入	为 <video> 或 <audio> 这类媒体元素指定媒体源 。
<track> 这个元素在 HTML5 中加入	为 <video> 或 <audio> 这类媒体元素指定文本轨道（字幕） 。
<canvas> 这个元素在 HTML5 中加入	代表位图区域 ，可以通过脚本在它上面实时呈现图形，如图表、游戏绘图等。
<map>	与 <area> 元素共同定义图像映射 区域。
<area>	与 <map> 元素共同定义图像映射 区域。
<svg> 这个元素在 HTML5 中加入	定义一个嵌入式矢量图 。
<math> 这个元素在 HTML5 中加入	定义一段数学公式 。
```
## 表格

``` stylus
Element	Description
<table>	定义多维数据 。
<caption>	代表表格的标题 。
<colgroup>	代表表格中一组单列或多列 。
<col>	代表表格中的列 。
<tbody>	代表表格中一块具体数据 （表格主体）。
<thead>	代表表格中一块列标签 （表头）。
<tfoot>	代表表格中一块列摘要 （表尾）。
<tr>	代表表格中的行 。
<td>	代表表格中的单元格 。
<th>	代表表格中的头部单元格 。
```
## 表单

``` stylus
Element	Description
<form>	代表一个表单 ，由控件组成。
<fieldset>	代表控件组 。
<legend>	代表 <fieldset> 控件组的标题 。
<label>	代表表单控件的标题 。
<input>	代表允许用户编辑数据的数据区 （文本框、单选框、复选框等）。
<button>	代表按钮 。
<select>	代表下拉框 。
<datalist> 这个元素在 HTML5 中加入	代表提供给其他控件的一组预定义选项 。
<optgroup>	代表一个选项分组 。
<option>	代表一个 <select> 元素或 <datalist> 元素中的一个选项
<textarea>	代表多行文本框 。
<keygen> 这个元素在 HTML5 中加入	代表一个密钥对生成器 控件。
<output> 这个元素在 HTML5 中加入	代表计算值 。
<progress> 这个元素在 HTML5 中加入	代表进度条 。
<meter> 这个元素在 HTML5 中加入	代表滑动条 。
```
## 交互元素

``` stylus

Element	Description
<details> 这个元素在 HTML5 中加入	代表一个用户可以(点击)获取额外信息或控件的小部件 。
<summary> 这个元素在 HTML5 中加入	代表 <details> 元素的综述 或标题 。
<menuitem> 这个元素在 HTML5 中加入	代表一个用户可以点击的菜单项。
<menu> 这个元素在 HTML5 中加入	代表菜单。
```


 

> Blockquote  [MDN][1]


  [1]: https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/HTML5/HTML5_element_list