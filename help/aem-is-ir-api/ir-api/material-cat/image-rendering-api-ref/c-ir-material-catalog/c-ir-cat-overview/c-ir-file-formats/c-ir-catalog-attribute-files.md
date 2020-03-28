---
description: 目录属性文件可以有任何名称，但必须有。ini文件后缀。 使用任何文本编辑器都可以轻松维护它们。
seo-description: 目录属性文件可以有任何名称，但必须有。ini文件后缀。 使用任何文本编辑器都可以轻松维护它们。
seo-title: 目录属性文件
solution: Experience Manager
title: 目录属性文件
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 目录属性文件{#catalog-attribute-files}

目录属性文件可以有任何名称，但必须有。ini文件后缀。 使用任何文本编辑器都可以轻松维护它们。

目录属性文件由一组文本记录组成，由单个 `<CR>` （ASCII代码0xD）、单个 `<LF>` （ASCII代码0xA）或一对文本记录 `<CR><LF>` 分隔。 每个记录都由一个属性名称和一个或多个以逗号分隔的属性值组成：

` *``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名称 </span></span> </p> </td> 
  <td class="stentry"> <p>属性名称；可以由一个或多个字母、数字、“-”和“_”组成；不区分大小写。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span></span> </p> </td> 
  <td class="stentry"> <p>属性值；除非在 <span class="codeph"> 换行符 </span>前使用单个反斜杠进行转义，否则不得包含 <span class="codeph"></span> &lt;CR&gt;或&lt;LF&gt;字符。 </p> </td> 
 </tr> 
</table>

* 令牌之间的空白是可选的。
* 具有未知属性名称的记录被平台服务器忽略。
* 属性名称可能由ASCII字母、数字以及“-”、“_”和“.”的任意组合组成
* 如果同一属性文件中出现同一属性名称多次，则最后一个遇到的名称优先。
* 使用“#”作为第一个字符将任何记录标记为分析器忽略的注释。

