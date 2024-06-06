---
title: 目录属性文件
description: 目录属性文件可以具有任何名称，但必须具有.ini文件后缀。 可以使用任何文本编辑器轻松维护它们。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# 目录属性文件{#catalog-attribute-files}

目录属性文件可以具有任何名称，但必须具有 `.ini` 文件后缀。 可以使用任何文本编辑器轻松维护它们。

目录属性文件由一组文本记录组成，用单个文件分隔 `<CR>` （ASCII代码0xD），单个 `<LF>` （ASCII代码0xA）或 `<CR><LF>` 配对。 每个记录由一个属性名称和一个或多个以逗号分隔的属性值组成：

`*`name`*= *`值`*&#42;[, *`值`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>属性名称；可能由一个或多个字母、数字、 — （连字符）和_（下划线）组成；不区分大小写。</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>属性值；不得包含 <span class="codeph"> &lt;cr&gt; </span>，或 <span class="codeph"> &lt;lf&gt; </span> 字符，除非在换行符之前用单个反斜杠转义。 </p> </td> 
 </tr> 
</table>

* 令牌之间的空格是可选的。
* 此 [!DNL Platform Server] 忽略具有未知属性名称的记录。
* 属性名称可以由ASCII字母、数字和 `-`， `_`、和 `.` 个字符。
* 如果同一属性文件中多次出现相同的属性名称，则最后一个出现的属性名称优先。
* 使用 `#` 作为第一个字符，用于将任何记录标记为解析器忽略的注释。
