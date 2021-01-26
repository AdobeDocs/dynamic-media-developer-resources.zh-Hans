---
description: 目录属性文件可以具有任何名称，但必须具有。ini文件后缀。 可以使用任何文本编辑器轻松地进行维护。
seo-description: 目录属性文件可以具有任何名称，但必须具有。ini文件后缀。 可以使用任何文本编辑器轻松地进行维护。
seo-title: 目录属性文件
solution: Experience Manager
title: 目录属性文件
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# 目录属性文件{#catalog-attribute-files}

目录属性文件可以具有任何名称，但必须具有。ini文件后缀。 可以使用任何文本编辑器轻松地进行维护。

目录属性文件由一组文本记录组成，由单个`<CR>`（ASCII代码`0xD`）、单个`<LF>`（ASCII代码`0xA`）或`<CR><LF>`对分隔。 每个记录都包含一个属性名称和一个或多个以逗号分隔的属性值：

`*`名`*= *`称值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> 值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>属性名称。 可以包含一个或多个字母、数字、-和_。 不区分大小写。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性值。 除非在换行符前用单个反斜杠进行转义，否则不得包含<span class="codeph"> &lt;CR&gt;</span>或<span class="codeph"> &lt;LF&gt;</span>字符。 </p></td> 
 </tr> 
</table>

令牌之间的空白是可选的。

平台服务器将忽略属性名称未知的记录。

属性名称可能由ASCII字母、数字以及“-”、“_”和“.”的任意组合组成。

如果同一属性文件中出现多个相同的属性名称，则最后一个遇到的名称优先。

使用#作为第一个字符将任何记录标记为注释，分析器将忽略该注释。
