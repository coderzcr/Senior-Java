# HTML基础

------

## HTML简介
　　HTML(HyperText Mark-up Language)中文名称为超文本标记语言，一种为普通文件中某些字句加上标识的语言，其目的在于运用标记（tag）合文件达到预期的效果。
　　
### HTML的优点

- HTML文件比较小，便于在网络上传输；
- HTML文档独立于计算机操作平台；
- 原则上，建立HTML文档不需要任何特殊的软件，只需一般的文本编辑器即可；
- HTML标记语言，非常便于学习。

### HTML的局限性
- 直接用文本编辑时，不是所见即所得；
- 不同浏览器对同一个HTML文档可能得到不同的显示效果；
- 已定义的标记往往不能满足多方面的需要。

## HTML基础标签
### HTML头部结构
#### DOCTYPE html
　　声明文档类型为HTML5文件。文档声明在HTML5文档必不可少，且必须放在文档的第一行。
#### meta
　　<meta> 标签提供了 HTML 文档的元数据。元数据不会显示在客户端，但是会被浏览器解析。META元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者及其他元数据。元数据可以被使用浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他 Web 服务调用。

属性 | 值 |  描述  
-|-|-
charset | character_set | 定义文档的字符编码。 |
content | text | 定义与 http-equiv 或 name 属性相关的元信息。 |
http-equiv | content-type</br>default-style</br>refresh | 把 content 属性关联到 HTTP 头部。 |
name | 	application-name</br>author</br>description</br>generator</br>keywords</br> | 把 content 属性关联到一个名称。 |

实例 1 - 定义文档关键词，用于搜索引擎：
```
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
```
实例 2 - 定义web页面描述：
```
<meta name="description" content="Free Web tutorials on HTML and CSS">
```
实例 3 - 定义页面作者：
```
<meta name="author" content="Hege Refsnes">
```
实例 4 - 每30秒刷新页面：
```
<meta http-equiv="refresh" content="30">
```

#### link

　　link标签定义文档与外部资源的关系。link标签最常见的用途是链接样式表。

<table><tr><th>属性</th>    <th>值</th>    <th>描述</th>  </tr><tr><td>charset</td>    <td>char_encoding</td>    <td><span> HTML5 不支持该属性。</span> 定义被链接文档的字符编码方式。</td>  </tr><tr><td>href</td>    <td>URL</td>    <td>定义被链接文档的位置。</td>  </tr><tr><td>hreflang</td>    <td>language_code</td>    <td>定义被链接文档中文本的语言。</td>  </tr><tr><td>media</td>    <td>media_query</td>    <td>规定被链接文档将显示在什么设备上。</td>      </tr><tr><td>rel</td>    <td>alternate<br>archives<br>author<br>bookmark<br>external<br>first<br>help<br>icon<br>last<br>license<br>next<br>nofollow<br>noreferrer<br>pingback<br>prefetch<br>prev<br>search<br>sidebar<br>stylesheet<br>tag<br>up</td>    <td>必需。定义当前文档与被链接文档之间的关系。</td>  </tr><tr><td>rev</td>    <td>reversed relationship</td>    <td><span> HTML5 不支持该属性。</span> 定义被链接文档与当前文档之间的关系。</td>  </tr><tr><td>sizes</td>    <td>HeightxWidth<br>any</td>    <td>定义了链接属性大小，只对属性 rel="icon" 起作用。</td>  </tr><tr><td>target</td>    <td>_blank<br>_self<br>_top<br>_parent<br>frame_name</td>    <td><span> HTML5 不支持该属性。</span> 定义在何处加载被链接文档。</td>  </tr><tr><td>type</td>    <td>MIME_type</td>    <td>规定被链接文档的 MIME 类型。</td>  </tr></table>

实例 
```
<head>
<link rel="stylesheet" type="text/css" href="styles.css">
</head>
```

#### title
　　标签定义文档的标题，在所有 HTML 文档中是必需的。

实例
```
<html>
<head>
<title>文档标题</title>
</head>
</html>
```

### 常见的块级标签
#### 常见的块级标签
标题标签`<h1></h1>...<h6></h6>`</br>
水平线`<hr/>`</br>
段落`<p></p>`</br>
换行`<br/>`</br>
引用`<blockquote</blockquote>`</br>
预格式`<pre></pre>` 可以保留您需要的文本格式，比如不会取消换行和空格，并且所示文本是等宽的。

#### ol(order list)
　　标签定义了一个有序列表. 列表排序以数字来显示。
<table><tbody><tr><th>属性</th><th>值</th><th>描述</th></tr><tr><td>compact</td><td>compact</td><td><span>HTML5中不支持，不赞成使用。</span>请使用样式取代它。规定列表呈现的效果比正常情况更小巧。</td></tr><tr><td>reversed</td><td>reversed</td><td>指定列表倒序(9,8,7...)</td></tr><tr><td>start</td><td>number</td><td>HTML5不支持，不赞成使用。请使用样式取代它。规定列表中的起始点。</td></tr><tr><td>type</td><td>1<br>A<br>a<br>I<br>i</td><td>规定列表的类型。不赞成使用。请使用样式代替。</td></tr></tbody></table>

实例
```
<ol>
 <li>咖啡</li>
 <li>茶</li>
 <li>牛奶</li>
</ol>
```
#### ul(unorder list)
　　标签定义了一个无序列表.
实例
```
<ul>
 <li>咖啡</li>
 <li>茶</li>
 <li>牛奶</li>
</ul>
```
#### 定义描述列表
　　`<dl>`标签定义一个描述列表。`<dl>`标签与 `<dt>`（定义项目/名字）和 `<dd>` 描述每一个项目/名字）一起使用。`<dl>`标签必须有开始标签和结束标签。

实例
```
<dl>
 <dt>Coffee</dt>
   <dd>Black hot drink</dd>
 <dt>Milk</dt>
   <dd>White cold drink</dd>
</dl> 
```

#### div
　　`<div>` 标签定义 HTML 文档中的一个分隔区块或者一个区域部分。`<div>` 元素经常与 CSS 一起使用，用来布局网页。

实例
```
<div style="color:#0000FF">
  <h3>这是一个在 div 元素中的标题。</h3>
  <p>这是一个在 div 元素中的文本。</p>
</div>
```