---
title: CSS  position 
tags: CSS
categories: web前端
---

CSS属性 position 用于指定一个元素在文档中的定位方式。top, right, bottom 和 left 属性则决定了该元素的最终位置。
# 文档流
- 将文档自上而下分成一行行， 并在每行中按从左至右的顺序排放元素，即为文档流。  
- 每个非浮动块级元素都独占一行，从上到下排列。 浮动元素则按规定浮在行的一端。 若当前行容不下， 则另起新行再浮动。 
- 内联元素从左往右排列，如果遇到阻碍自动换行
- 脱离文档流的方式：浮动，绝对定位， 固定定位。
# 主要参数
## absolute 
生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。 元素的位置通过 “left”, “top”, “right” 以及 “bottom” 属性进行规定。它会脱离文档流。 
## fixed 
生成绝对定位的元素，相对于浏览器窗口进行定位。 元素的位置通过 “left”, “top”, “right” 以及 “bottom” 属性进行规定。 它会脱离文档流
## relative 
生成相对定位的元素， 相对自己文档流中的原始位置定位，不会脱离文档流。使用position:relative定位，其元素依旧在文档流中，他的位置可以使用 left、right、top、bottom、z-index等定位参数。列如：”left:10” 会向元素的 LEFT 位置添加 20 像素。 
## sticky
粘性定位是相对定位和固定定位的混合。元素在跨越特定阈值前为相对定位，之后为固定定位。须指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。
## static 
默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。 
