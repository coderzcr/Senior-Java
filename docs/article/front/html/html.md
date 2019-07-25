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

### 常见的行级标签

#### 常见的行级标签

span 文本 : 用于包裹一部分文字，进行特定样式的修改。</br>
```
小明真<span style="color:red; font-size:36px;">酷</span>！！
```
img 图片 </br>
em 强调：浏览器显示为倾斜 </br>
strong 强调：浏览器显示为加粗。 </br>
q 短引用 </br>
a 超链接 </br>
i 倾斜 </br>
b 加粗 </br>
small 缩小字体 </br>
u 下划线 </br>

#### q
　　标签定义一个短的引用。浏览器经常会在这种引用的周围插入引号。
<table>
        <tbody>
            <tr>
                <th>属性</th>
                <th>值</th>
                <th>描述</th>
            </tr>
            <tr>
                <td>cite</td>
                <td>URL</td>
                <td>规定引用的源 URL。</td>
            </tr>
        </tbody>
    </table>

实例
```
<p>WWF's goal is to: 
<q>Build a future where people live in harmony with nature.</q> 
We hope they succeed.</p>
```
#### img
　　标签用于展示 HTML 页面中的图像，使得页面能够“图文并茂”。img标签有两个必需的属性：src 和 alt。
<table>   <tbody><tr>    <th>属性</th>    <th>值</th>    <th>描述</th>  </tr>  <tr>    <td>align</td>    <td>top<br>      bottom<br>      middle<br>      left<br>      right</td>    <td><span>HTML5 不支持。HTML 4.01 已废弃。</span>    规定如何根据周围的文本来排列图像。</td>      </tr>  <tr>    <td>alt</td>    <td><em>text</em></td>    <td>规定图像的替代文本。</td>  </tr>  <tr>    <td>border</td>    <td><em>pixels</em></td>    <td><span>HTML5 不支持。HTML 4.01 已废弃。</span>    规定图像周围的边框。</td>  </tr>      <tr>    <td>crossorigin</td>    <td>anonymous <br>use-credentials</td>    <td>设置图像的跨域属性</td>        </tr>      <tr>    <td>height</td>    <td><em>pixels</em></td>    <td>规定图像的高度。</td>        </tr>        <tr>    <td>hspace</td>    <td><em>pixels</em></td>    <td><span>HTML5 不支持。HTML 4.01 已废弃。</span>    规定图像左侧和右侧的空白。</td>        </tr>        <tr>    <td>ismap</td>    <td>ismap</td>    <td>将图像规定为服务器端图像映射。</td>        </tr>  <tr>    <td>longdesc</td>    <td><em>URL</em></td>    <td><span>HTML5 不支持。HTML 4.01 已废弃。</span>    指向包含长的图像描述文档的 URL。</td>  </tr>        <tr>    <td>src</td>    <td><em>URL</em></td>    <td>规定显示图像的 URL。</td>  </tr>        <tr>    <td>usemap</td>   <td><em>#mapname</em></td>    <td>将图像定义为客户器端图像映射。</td>        </tr>  <tr>    <td>vspace</td>    <td><em>pixels</em></td>    <td><span>HTML5 不支持。HTML 4.01 已废弃。</span>    规定图像顶部和底部的空白。</td>  </tr>  <tr>    <td>width</td>    <td><em>pixels</em></td>    <td>规定图像的宽度。</td>  </tr>  </tbody></table>
实例

```
<img src="smiley.gif" alt="Smiley face" height="42" width="42">
```
### 表格标签

#### table

`<table></table>`表格框</br>
`<tr></tr>`表格行</br>
`<td></td>`表格列</br>
`<th></th>` 表格标题列（将tr中的td替换为th)，th默认加粗且在单元格居中显示。

#### table属性

属性 | 值 |  描述  
-|-|-
align|left</br>center</br>right|HTML5 不支持。HTML 4.01 已废弃。 规定表格相对周围元素的对齐方式。
bgcolor|	rgb(x,x,x)</br>#xxxxxx</br>colorname|HTML5 不支持。HTML 4.01 已废弃。 规定表格的背景颜色。
border|	1</br>""|规定表格单元是否拥有边框。
cellpadding	|pixels|	HTML5 不支持。规定单元边沿与其内容之间的空白。
cellspacing	|pixels|	HTML5 不支持。规定单元格之间的空白。
frame|	void</br>above</br>below</br>hsides</br>lhs</br>rhs</br>vsides</br>box</br>border|HTML5 不支持。规定外侧边框的哪个部分是可见的。
rules|none</br>groups</br>rows</br>cols</br>all	|HTML5 不支持。规定内侧边框的哪个部分是可见的。
summary	|text|	HTML5 不支持。规定表格的摘要。
width|	pixels</br>%|HTML5 不支持。规定表格的宽度。

实例-1 一个简单的 HTML 表格，包含两列两行：

```
<table border="1">
<tr>
<th>Month</th>
<th>Savings</th>
</tr>
<tr>
<td>January</td>
<td>$100</td>
</tr>
</table>
```

#### table多列与多行
跨列：colspan，某单元格跨N列，则该单元格右边的N-1个td就不需要了。
跨行：rowspan，某单元格跨N行，则该单元格下边的N-1个td就不需要了。

实例-2 表格单元横跨两列的表格

```
<table width="100%" border="1">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td colspan="2">January</td>
  </tr>
  <tr>
    <td colspan="2">February</td>
  </tr>
</table>
```

实例-3 表格单元竖跨两列的表格

```
<table border="1">
  <tr>
    <td rowspan="2">星期一</td>
    <td>星期二</td>
  </tr>
  <tr>
    <td>星期三</td>
  </tr>
</table>
```

### 表单标签

#### 表单语法
　　HTML 表单用于搜集不同类型的用户输入
实例-1 form基本使用 method规定如何发送表单数据,常用值：get|post。action表示向何处发送表单数据

```
<form method="post" action="result.html">
   <p>名字：<input name="name" type="text" ></p>
   <p>密码：<input name="pass" type="password"></p>
   <p>
      <input type="submit" name="Button" value="提交"/>
      <input type="reset" name="Reset" value="重填"/> 
    </p>
</form>
```

#### 常用表单元素

input 表单元素，表单项</br>

<table>
        <tbody>
            <tr>
                <th>属性</th>
                <th>值</th>
                <th>描述</th>
            </tr>
            <tr>
                <td rowspan="10">type</td>
                <td>text</td>
                <td>单行文本输入框</td>
            </tr>
            <tr>
                <td>password</td>
                <td>密码输入框</td>
            </tr>
            <tr>
                <td>checkbox</td>
                <td>复选框</td>
            </tr>
            <tr>
                <td>radio</td>
                <td>单选框</td>
            </tr>
            <tr>
                <td>file</td>
                <td>文件域</td>
            </tr>
            <tr>
                <td>submit</td>
                <td>将表单里的信息提交给表单属性action所指向的文件</td>
            </tr>
            <tr>
                <td>reset</td>
                <td>清空表单信息</td>
            </tr>
            <tr>
                <td>image</td>
                <td>图片提交按钮</td>
            </tr>
            <tr>
                <td>button</td>
                <td>按钮</td>
            </tr>
            <tr>
                <td>hidden</td>
                <td>隐藏域</td>
            </tr>
        </tbody>
    </table>

实例-1 文本框
```
<input  type="text"(文本框)  name="userName"(文本框名称) value="用户名"(文本框初始值) size="30"(文本框长度) maxlength="20"(文本框可输入最多字符) />
```

实例-2 密码框
```
<input  type="password "(密码框)  name="pass"(密码框的名称)  size="20"(密码框的长度) />
```

实例-3 单选按钮
```
<input name="gen" type="radio"(单选按钮框) value="男"(值)  checked(单选按钮选中状态)  />男
<input name="gen" type="radio" value="女" />女
```

实例-4 复选框
```
<input type="checkbox"(复选框) name="interest" value="sports"(值)/>运动
<input type="checkbox" name="interest" value="talk" checked(复选框选中状态) />聊天
<input type="checkbox" name="interest" value="play"/>玩游戏
```
实例-5 按钮
```
<input type="reset" (重置按钮) name="butReset"  value="reset按钮"(按钮上显示的文字)>
<input type="submit"(提交按钮) name="butSubmit" value="submit按钮">
<input type="button"(普通按钮) name="butButton" value="button按钮"/>
<input type="image"(图片按钮) src="images/login.gif"/(图片路径)>
```

实例-6 文件域
```
<form action="" method="post" enctype="multipart/form-data"（表单编码属性）>
  <p><input type="file"(文件域) name="files" />
  <input type="submit" name="upload" value="上传" /></p>
</form>
```

实例-7 邮件 (会自动验证Email地址格式是否正确)
```
<p>邮箱:<input type="email"（邮箱）  name="email"/></p>
<input type="submit"/>
```

实例-8 网址(会自动验证网址格式是否正确)
```
<p>请输入你的网址:<input type="url"（网址）  name="userUrl"/></p>
<input type="submit"/>
```

实例-9 数字
```
<p>请输入数字:<input type="number"(数字)  name="num" min="0"(允许的最小值) max="100"(允许的最大值) step(合法的数字间隔)="10"/></p>
<input type="submit"/>
```

实例-10 滑块
```
<p>请输入数字:<input type="range"(滑块)  name="range1" min="0"(允许的最小值) max="10"(允许的最大值) step(合法的数字间隔)="2"/></p>
<input type="submit"/>
```
实例-11 搜索框
```
<p>请输入搜索的关键词:<input type="search"(搜索框)  name="sousuo"/></p>
<input type="submit"/>
```

select和option 下拉菜单</br>
实例
```
<select(列表框) name="列表名称" size="行数">
<option value="选项的值" selected="selected"(默认选中项)>…</option >
<option(选项) value="选项的值">…</option >
</select>
```

textarea 文本域</br>

实例
```
<textarea(多行文本域)  name="showText"  cols="x"(显示的列数)  rows="y"(显示的行数)>文本内容 </textarea  >
```
