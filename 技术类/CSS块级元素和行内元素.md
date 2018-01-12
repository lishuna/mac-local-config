块级元素
====

HTML（超文本标记语言）中元素大多数都是“块级”元素或[行内元素](https://developer.mozilla.org/zh-CN/docs/HTML/Inline_elements "/zh-CN/docs/HTML/Inline_elements")。块级元素占据其父元素（容器）的整个空间，因此创建了一个“块”。通常浏览器会在块级元素前后另起一个新行。

内容模型一般块级元素可以包含行内元素和其他块级元素。这种结构上的包含继承区别可以使块级元素创建比行内元素更”大型“的结构。

元素列表[EDIT](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Block-level_elements$edit#元素列表)
--------------------------------------------------------------------------------------------

以下是 HTML 中所有的块级元素列表（虽然”块级“在新的 HTML5 元素中没有明确定义）

[`<address>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/address "HTML 的<address>元素可以让作者为它最近的<article>或者<body>祖先元素提供联系信息。在后一种情况下，它应用于整个文档。")联系方式信息。[`<article>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article "<article>元素表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)文章内容。[`<aside>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/aside "<aside> 元素中连接到页面中其他部分的内容，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。其通常表现为侧边栏或者被插入在该内容里。他们通常包含在工具条，例如来自词汇表的定义。也可能有其他类型的信息，例如相关的广告、笔者的传记、web 应用程序、个人资料信息，或在博客上的相关链接。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)伴随内容。[`<audio>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio "HTML <audio> 元素用于在文档中表示音频内容。 <audio> 元素可以包含多个音频资源， 这些音频资源可以使用 src 属性或者<source> 元素来进行描述； 浏览器将会选择最合适的一个来使用。对于不支持<audio>元素的浏览器，<audio>元素也可以作为浏览器不识别的内容加入到文档中。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)音频播放。[`<blockquote>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/blockquote "HTML中的元素（或者 HTML 块级引用元素），代表其中的文字是引用内容。通常在渲染时，这部分的内容会有一定的缩进（注 中说明了如何更改）。若引文来源于网络，则可以将原内容的出处 URL 地址设置到 cite 特性上，若要以文本的形式告知读者引文的出处时，可以通过 <cite> 元素。")块引用。[`<canvas>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/canvas "<canvas>元素可被用来通过脚本（通常是JavaScript）绘制图形。比如,它可以被用来绘制图形,制作图片集合,甚至用来实现动画效果。你可以(也应该)在元素标签内写入可提供替代的的代码内容，这些内容将会在在旧的、不支持<canvas>元素的浏览器或是禁用了JavaScript的浏览器内渲染并展现。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)绘制图形。[`<dd>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dd "HTML <dd> 元素（HTML 描述元素）用来指明一个描述列表  (<dl>) 元素中一个术语的描述。这个元素只能作为描述列表元素的子元素出现，并且必须跟着一个 <dt> 元素。")定义列表中定义条目描述。[`<div>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div "HTML <div> 元素 (或 HTML 文档分区元素) 是一个通用型的流内容容器，它在语义上不代表任何特定类型的内容，它可以被用来对其它元素进行分组，一般用于样式化相关的需求（使用 class 或 id 特性) 或者对具有相同特性的一组元素进行分组 (比如 lang)，它应该在没有任何其它语义元素可用是才使用 (比如 <article> 或 <nav>) 。")文档分区。[`<dl>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dl "HTML <dl> 元素 （或 HTML 描述列表元素）是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键-值对列表)。")定义列表。[`<fieldset>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/fieldset "此页面仍未被本地化, 期待您的翻译!")表单元素分组。[`<figcaption>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figcaption "此页面仍未被本地化, 期待您的翻译!") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)图文信息组标题[`<figure>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figure "此页面仍未被本地化, 期待您的翻译!") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)图文信息组 (参照 [`<figcaption>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/figcaption "此页面仍未被本地化, 期待您的翻译!"))。[`<footer>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer "HTML footer元素() 表示最近一个章节内容或者根节点元素的页脚。一个页脚通常包含该章节作者、版权数据或者与文档相关的链接等信息。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)区段尾或页尾。[`<form>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/form "HTML <form> 元素 表示了文档中的一个区域，这个区域包含有交互控制元件，用来向web服务器提交信息。")表单。[`<h1>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h1 "此页面仍未被本地化, 期待您的翻译!"), [`<h2>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h2 "此页面仍未被本地化, 期待您的翻译!"), [`<h3>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h3 "此页面仍未被本地化, 期待您的翻译!"), [`<h4>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h4 "此页面仍未被本地化, 期待您的翻译!"), [`<h5>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h5 "此页面仍未被本地化, 期待您的翻译!"), [`<h6>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h6 "此页面仍未被本地化, 期待您的翻译!")标题级别 1-6.[`<header>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header "<header>元素表示一组引导性的帮助，可能包含标题元素，也可以包含其他元素，像logo、分节头部、搜索表单等。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)区段头或页头。[`<hgroup>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/hgroup "此页面仍未被本地化, 期待您的翻译!") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)标题组。[`<hr>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/hr "The HTML <hr> element represents a thematic break between paragraph-level elements (for example, a change of scene in a story, or a shift of topic with a section). In previous versions of HTML, it represented a horizontal rule. It may still be displayed as a horizontal rule in visual browsers, but is now defined in semantic terms, rather than presentational terms.")水平分割线。
[`<noscript>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/noscript "<noscript> 标签 当某个script类型在浏览器中不受支持或者被关闭时作为替代的内容")不支持脚本或禁用脚本时显示的内容。[`<ol>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol "The HTML <ol> Element (or HTML Ordered List Element) represents an ordered list of items. Typically, ordered-list items are displayed with a preceding numbering, which can be of any form, like numerals, letters or Romans numerals or even simple bullets. This numbered style is not defined in the HTML description of the page, but in its associated CSS, using the list-style-type property.")有序列表。[`<output>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/output "HTML 标签定义一个用户的操作或者计算的结果。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)表单输出。[`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p "HTML的元素（或者HTML段落元素）表示一个段落。段落是")行。[`<pre>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre "HTML格式化文本（）代表预格式化文本。在该元素中的文本通常以非比例的字体显示出来，正如文件中所显示的那样。这里面的元素显示为输入空格。")预格式化文本。[`<section>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section "HTML Section 元素 (<section>) 表示文档中的一个区域（或节），比如，内容中的一个专题组，一般来说会有包含一个 heading。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)一个页面区段。[`<table>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table "HTML中table标签 (<table>) 用来展示多行的数据。")表格。[`<tfoot>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tfoot "此页面仍未被本地化, 期待您的翻译!")表脚注。[`<ul>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul "此页面仍未被本地化, 期待您的翻译!")无序列表。[`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video "HTML <video> 元素 用于在HTML或者XHTML文档中嵌入视频内容。") [HTML5](https://developer.mozilla.org/zh-CN/docs/HTML/HTML5)视频。

行内元素
====

一个行内元素只占据它对应标签的边框所包含的空间。一般情况下，行内元素只能包含数据和其他行内元素。默认情况下，行内元素不会以新行开始，而块级元素会新起一行。

行内元素列表[EDIT](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Inline_elemente$edit#Elements)
---------------------------------------------------------------------------------------------

下面的元素都是行内元素：

* [b](https://developer.mozilla.org/zh-CN/HTML/Element/b "zh-CN/HTML/Element/b"), [big](https://developer.mozilla.org/zh-CN/HTML/Element/big "zh-CN/HTML/Element/big"), [i](https://developer.mozilla.org/zh-CN/HTML/Element/i "zh-CN/HTML/Element/i"), [small](https://developer.mozilla.org/zh-CN/HTML/Element/small "zh-CN/HTML/Element/small"), [tt](https://developer.mozilla.org/zh-CN/HTML/Element/tt "zh-CN/HTML/Element/tt")
* [abbr](https://developer.mozilla.org/zh-CN/HTML/Element/abbr "zh-CN/HTML/Element/abbr"), [acronym](https://developer.mozilla.org/zh-CN/HTML/Element/acronym "zh-CN/HTML/Element/acronym"), [cite](https://developer.mozilla.org/zh-CN/HTML/Element/cite "zh-CN/HTML/Element/cite"), [code](https://developer.mozilla.org/zh-CN/HTML/Element/code "zh-CN/HTML/Element/code"), [dfn](https://developer.mozilla.org/zh-CN/HTML/Element/dfn "zh-CN/HTML/Element/dfn"), [em](https://developer.mozilla.org/zh-CN/HTML/Element/em "zh-CN/HTML/Element/em"), [kbd](https://developer.mozilla.org/zh-CN/HTML/Element/kbd "zh-CN/HTML/Element/kbd"), [strong](https://developer.mozilla.org/zh-CN/HTML/Element/strong "zh-CN/HTML/Element/strong"), [samp](https://developer.mozilla.org/zh-CN/HTML/Element/samp "zh-CN/HTML/Element/samp"), [var](https://developer.mozilla.org/zh-CN/HTML/Element/var "zh-CN/HTML/Element/var")
* [a](https://developer.mozilla.org/zh-CN/HTML/Element/a "zh-CN/HTML/Element/a"), [bdo](https://developer.mozilla.org/zh-CN/HTML/Element/bdo "zh-CN/HTML/Element/bdo"), [br](https://developer.mozilla.org/zh-CN/HTML/Element/br "zh-CN/HTML/Element/br"), [img](https://developer.mozilla.org/zh-CN/HTML/Element/Img "zh-CN/HTML/Element/Img"), [map](https://developer.mozilla.org/zh-CN/HTML/Element/map "zh-CN/HTML/Element/map"), [object](https://developer.mozilla.org/zh-CN/HTML/Element/object "zh-CN/HTML/Element/object"), [q](https://developer.mozilla.org/zh-CN/HTML/Element/q "zh-CN/HTML/Element/q"), [script](https://developer.mozilla.org/zh-CN/HTML/Element/Script "zh-CN/HTML/Element/Script"), [span](https://developer.mozilla.org/zh-CN/HTML/Element/span "zh-CN/HTML/Element/span"), [sub](https://developer.mozilla.org/zh-CN/HTML/Element/sub "zh-CN/HTML/Element/sub"), [sup](https://developer.mozilla.org/zh-CN/HTML/Element/sup "zh-CN/HTML/Element/sup")
* [button](https://developer.mozilla.org/zh-CN/HTML/Element/button "zh-CN/HTML/Element/button"), [input](https://developer.mozilla.org/zh-CN/HTML/Element/Input "zh-CN/HTML/Element/Input"), [label](https://developer.mozilla.org/zh-CN/HTML/Element/label "zh-CN/HTML/Element/label"), [select](https://developer.mozilla.org/zh-CN/HTML/Element/select "zh-CN/HTML/Element/select"), [textarea](https://developer.mozilla.org/zh-CN/HTML/Element/textarea "zh-CN/HTML/Element/textarea")

### 三、block（块）元素的特点:

①、总是在新行上开始；
②、高度，行高以及外边距和内边距都可控制；
③、宽度缺省是它的容器的100%，除非设定一个宽度。
④、它可以容纳内联元素和其他块元素

### [](http://jeffjade.com/2015/06/24/2015-06-24-css-block-inline/#四、inline元素的特点 "四、inline元素的特点")四、inline元素的特点

①、和其他元素都在一行上；
②、高，行高及外边距和内边距不可改变；
③、宽度就是它的文字或图片的宽度，不可改变
④、内联元素只能容纳文本或者其他内联元素
对行内元素，需要注意如下

> 设置宽度width 无效。
> 设置高度height 无效，可以通过line-height来设置。
> 设置margin 只有左右margin有效，上下无效。
> 设置padding只有左右padding有效，上下则无效。注意元素范围是增大了，但是对元素周围的内容是没影响的。
> 
> ### 行内元素与块级元素有什么不同？
> 
> 区别一：
> 块级：块级元素会独占一行，默认情况下宽度自动填满其父元素宽度
> 行内：行内元素不会独占一行，相邻的行内元素会排在同一行。其宽度随内容的变化而变化。
> 
> 区别二：
> 块级：块级元素可以设置宽高
> 行内：行内元素不可以设置宽高
> 
> 区别三：
> 块级：块级元素可以设置margin，padding
> 行内：行内元素水平方向的margin-left; margin-right; padding-left; padding-right;可以生效。但是竖直方向的margin-bottom; margin-top; padding-top; padding-bottom;却不能生效。
> 
> 区别四：
> 块级：display:block;
> 行内：display:inline;
> 可以通过修改display属性来切换块级元素和行内元素