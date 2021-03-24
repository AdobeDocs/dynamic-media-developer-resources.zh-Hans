---
description: 目录属性文件可以具有任何名称，但必须具有.ini文件后缀。 可以使用任何文本编辑器随时进行维护。
solution: Experience Manager
title: 目录属性文件
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# 目录属性文件{#catalog-attribute-files}

目录属性文件可以具有任何名称，但必须具有.ini文件后缀。 可以使用任何文本编辑器随时进行维护。

目录属性文件由一组文本记录组成，由单个`<CR>`（ASCII代码0xD）、单个`<LF>`（ASCII代码0xA）或`<CR><LF>`对分隔。 每个记录都包含一个属性名称和一个或多个以逗号分隔的属性值：

`*``*= *``*&#42;[, *`namevaluevalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名称  </span> </span> </p> </td> 
  <td class="stentry"> <p>属性名称；可以包含一个或多个字母、数字、“ — ”和“_”；不区分大小写。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>属性值；不得包含<span class="codeph"> &lt;CR&gt; </span>或<span class="codeph"> &lt;LF&gt; </span>字符，除非在换行符前使用单个反斜杠进行转义。 </p> </td> 
 </tr> 
</table>

* 令牌之间的空格是可选的。
* 平台服务器将忽略属性名称未知的记录。
* 属性名称可能由ASCII字母、数字以及“ — ”、“_”和“。”的任意组合组成。
* 如果同一属性文件中出现多次同一属性名称，则最后一个名称优先。
* 使用“#”作为第一个字符，将任何记录标记为解析器忽略的注释。

