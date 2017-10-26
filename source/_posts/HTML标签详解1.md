---
title: HTML5标签详解（1）
tags: HTML
categories: web前端
---
# **< a >** 标签
**< a >** 元素  (或锚元素) 创建一个到其他网页，文件，同一页面内的位置，电子邮件地址或任何其他URL的超链接。（发起HTTP GET请求）。

``` stylus
<a href="http://qq.com"></a>
```
### target属性
``` stylus
<a href="http://qq.com" target=_blank>QQ</a>   <!--在新窗口打开-->
<a href="http://qq.com" target=_self>QQ</a>      <!--在当前窗口打开-->
<a href="http://qq.com" target=_parent>QQ</a>  <!--在父级窗口打开-->
<a href="http://qq.com" target=_top>QQ</a>       <!--在顶级窗口打开-->
```

 - _ self:当前页面加载，此值是默认的，如果没有指定属性的话。
 - _blank: 新窗口打开，即到一个新的未命名的窗口。
 - _parent:加载响应到当前窗口的父级窗口。如果没有，此选项的行为方式相同_self。
 - _top:加载响应到祖级窗口，如果没有，此选项的行为方式相同_self。
### download 属性
此属性指示浏览器下载URL而不是解析URL，因此将提示用户将其保存为本地文件。
不用download属性的情况下，是否会下载由http响应决定，如果content-type:application/octet-stream,那么浏览器会以下载的形式接受请求。
### href属性

``` stylus
href="qq.com"    <!--不会跳转到qq主页，会打开名为qq.com的文件或者相对路径./qq.com-->
href="http://qq.com"<!--正确写法，会跳转打开qq主页-->
href="//qq.com"<!--无协议绝对地址，自动继承协议，当前页面是什么协议就用什么协议-->
href="#top"     <!--回到页面顶部-->
href="#xxxx"   <!--锚点发起页面内的跳转，xxx为ID，不发起get请求-->
href="?name=xxx"<!--会发起get请求-->
href=“javascript:alert(1);”   <!--js伪协议，会直接执行js代码-->
href=“javascript:;”   <!--无任何反应-->
href=""  <!--跳转自身，刷新页面-->
```
href的值还可以是相对路径。URL不限于网页（HTTP）的文件。URL可能使用浏览器所支持的任何协议。例如，文件，FTP，大多数用户代理mailto工作。

# **< iframe >** 标签

HTML内联框架元素 <frame 表示嵌套的浏览上下文，有效地将另一个HTML页面嵌入到当前页面中。
列如：
``` stylus
<iframe src="http://qq.com" frameborder="0"></iframe>
```
这会在当前页面嵌入一个qq的主页，默认width：100；height：50。可用CSS改变。

### name属性

嵌入的浏览上下文（框架）的名称。该名称可以用作`<a>`标签，`<form>`标签的target属性值，或`<input> `标签和` <button>`标签的formtaget属性值。

``` stylus
<iframe name=xxx src="#" frameborder="0"></iframe>
<a target=xxx href="http://qq.com">点击QQ</a>
```
这会在iframe窗口打开qq主页

### frameborder属性
iframe默认会有一个border（边框），当frameborder=0时，可以去掉边框。
### src属性
嵌套页面的URL地址；也可以是相对路径。
# **< input >** 标签
< input > 标签用于为基于Web的表单创建交互式控件，以便接受来自用户的数据。
### type属性
``` stylus
<input type="button" value="button">
<!--只是一个按钮，不能提交 -->

<input type="checkbox" name="fruit" value="apple">苹果
<!--复选框-->

<input type="checkbox" id=xxx><label for="xxx">选我</label>
<label><input type="checkbox">选我<\label>
<!--以上两种写法可以直接点击“选我”选中复选框 -->

<input type="radio" name="fruit" value="apple">苹果
<!--单选框，name值要相同才能实现单选-->


```

1.button：无行为按钮。
2.checkbox： 复选框。必须使用 value 属性定义此控件被提交时的值。使用 checked 属性指示控件是否被选择。也可以使用 
3. color：HTML5 用于指定颜色的控件。
4. date：HTML5 用于输入日期的控件（年，月，日，不包括时间）。
5. datetime：HTML5 基于 UTC 时区的日期时间输入控件（时，分，秒及几分之一秒）。
6. datetime-local：HTML5 用于输入日期时间控件，不包含时区。
7.email：HTML5 用于编辑 e-mail 的字段。 合适的时候可以使用 :valid 和 :invalid CSS 伪类。
8. file：此控件可以让用户选择文件。使用 accept 属性可以定义控件可以选择的文件类型。
9. hidden：不显示在页面上的控件，但它的值会被提交到服务器。
10. image：图片提交按钮。必须使用 src 属性定义图片的来源及使用 alt 定义替代文本。还可以使用 height 和 width 属性以像素为单位定义图片的大小。
11. month：HTML5 用于输入年月的控件，不带时区。
12. number: HTML5 用于输入浮点数的控件。
13. password：一个值被遮盖的单行文本字段。使用 maxlength 指定可以输入的值的最大长度 。
14. radio：单选按钮。必须使用 value 属性定义此控件被提交时的值。使用checked 必须指示控件是否缺省被选择。在同一个”单选按钮组“中，所有单选按钮的 name 属性使用同一个值； 一个单选按钮组中是，同一时间只有一个单选按钮可以被选择。
15. range：HTML5 用于输入不精确值控件。如果未指定相应的属性，控件使用如下缺省值：
- min：0
- max：100
- value：min + (max-min)/2，或当 max 小于 min 时使用 min
- step：1
16. reset：用于将表单所内容设置为缺省值的按钮。
17. search：HTML5用于输入搜索字符串的单行文本字段。换行会被从输入的值中自动移除。
18. submit：用于提交表单的按钮。
19. tel：HTML5 用于输入电话号码的控件。
20. text：单行字段；换行会将自动从输入的值中移除。
21. me：HTML5 用于输入不含时区的时间控件。
22. url：HTML5 用于编辑URL的字段。 T
23. week：HTML5 用于输入一个由星期-年组成的日期，日期不包括时区。

# **< select >** 标签
下拉列表，是一种表单控件，可创建选项菜单。菜单内的选项为< option > , 可以由 < optgroup > 元素分组。选项可以被用户预先选择。

``` stylus
<select name="group" multiple><!--multiple可以实现按shift多选-->
   <option value="">空</option><!--value为空-->
   <option value="1" disabled>第一</option><!--不可选-->
   <option value="2">第二</option><!---->
   <option value="3" selected>第三</option><!--默认选中-->
 </select>
```
包括下列全局属性：

### autofocus
这个属性能够让一个对象在页面加载的时候获得焦点. 在一个页面上下文中, 只有一个对象可以有这个属性，并且是布尔值(true 或者 false)。

### disabled
这个布尔值的属性表明一个用户是否可以操控该表单对象. 

### form
select所关联的form表单 (它的"表单拥有者"). 如果这个属性被明确定义, 那么它的值一定是在同一个document中表单ID. 这样能够让你把select标签放在任何的位置, 不仅限于作为form表单的后代元素。

### multiple
这个布尔值的属性标记select是否可以多选. 默认是单选。

### name
控件名称。
### required
规定select的值不能为空(布尔值)。
### size
如果控件显示为滚动列表框，则此属性表示为控件中同时可见的行数。浏览器不需要将选择元素呈现为滚动列表框。默认值为0。

# < textarea > 标签

表示一个多行纯文本编辑控件,可用css改变可控制文本框的大小，设置style="resize:none"可使文本框固定，不能随意拉动
```stylus
<textarea name="textarea" rows="10" cols="50">Write something here</textarea>

```
包含了全局属性：
### cols
文本域的可是宽度。必须为正数，默认为20 (HTML5)。
### resize:none
去掉文本域右下角的默认的灰色斜杠。
### disabled
禁用文本域。默认为false。如果未指定，也可以从父级上如< fieldset >继承而来。
### form
指定跟自身相关联的表单。值必须为本文档内的表单的ID，如果未指定，就是跟当前所在的表单元素相关联。这就允许你在文档的任意地方放置文本域元素。
### maxlength 
允许用户输入的最大字符长度 (Unicode) 。未指定表示无限长度。
### minlength 
允许用户输入的最小字符长度(Unicode) 
### name
元素的名称。
### placeholder
占位符，用来提示用户进行内容输入。
### readonly
不允许用户修改元素内文本。和 disabled 属性不同的是，这个能让用户点击和选择元素内的文本。如果在表单里，这个元素的值还是会跟随表单一起提交。
### required 
提示用户这个元素的内容必填。
### rows
元素的输入文本的行数（显示的高度）。
### autocomplete HTML5
是否使用浏览器的记忆功能自动填充文本。可能的值有：
- off: 不使用浏览器的记忆自动填充，使用者必须输入他们想要输入的所有内容。或者网页提供了自己的自动填充方法。
- on: 浏览器根据用户之前输入的内容或者习惯，在用户输入的时候给出相应输入提示。

# **< form >** 标签

表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。（发起HTTP POST请求）。

``` stylus
<form action="" method="post" target="">
        <input type="submit" value="提交">
    </form>
```
 1. 如果form表单里面没有提交按钮就无法提交form,除非用js。
 2. method=post: 指的是 HTTP POST 方法 ; 表单数据会包含在表单体内然后发送给服务器.(当URI action是以 '?' 作为分隔符的查询参数时，会发起get请求)。method=get: 指的是 HTTP GET 方法; 表单数据会附加在 URI action 属性中并以 '?' 作为分隔符, 然后这样得到的 URI 再发送给服务器. （建议直接用< a >标签)
 3. 当没有method属性时，默认为GET
 4. target属性与< a >标签类似
### 列子：

``` stylus
<!-- 一个简单的表单，这个表单会发送一个 GET 请求 -->
<form action="">
  <label for="GET-name">Name:</label>
  <input id="GET-name" type="text" name="name"><!-- name的值会作为post请求的第四部分被提交 -->
  <input type="submit" value="Save">
</form>

```

``` stylus
<!-- 一个简单的表单，发送 POST 请求 -->
<form action="" method="post">
  <label for="POST-name">Name:</label>
  <input id="POST-name" type="text" name="name">
  <input type="submit" value="Save">
</form>
```


[未完待续 < table >][1]


  [1]: https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table