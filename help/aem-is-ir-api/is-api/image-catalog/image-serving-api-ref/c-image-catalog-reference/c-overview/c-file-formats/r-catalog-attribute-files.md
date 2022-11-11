---
description: 目录属性文件可以具有任何名称，但必须具有.ini文件后缀。 使用任何文本编辑器都可以轻松地维护它们。
solution: Experience Manager
title: 目录属性文件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# 目录属性文件{#catalog-attribute-files}

目录属性文件可以具有任何名称，但必须具有.ini文件后缀。 使用任何文本编辑器都可以轻松地维护它们。

目录属性文件由一组文本记录组成，并以单个 `<CR>` (ASCII代码 `0xD`), `<LF>` (ASCII代码 `0xA`)或a `<CR><LF>` 配对。 每个记录都包含一个属性名称和一个或多个以逗号分隔的属性值：

`*`name`*= *`值`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> 值</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>属性名称。 可以包含一个或多个字母、数字、 — 和_。 不区分大小写。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>属性值。 不得包括 <span class="codeph"> &lt;cr&gt;</span> 或 <span class="codeph"> &lt;lf&gt;</span> 字符，除非在换行符之前使用单个反斜杠进行转义。 </p></td> 
 </tr> 
</table>

令牌之间的空格是可选的。

属性名称未知的记录将被 [!DNL Platform Server].

属性名称可以由ASCII字母、数字以及“ — ”、“_”和“。”的任意组合组成。

如果同一属性文件中出现同一属性名称多次，则最后一次出现的属性名称优先。

使用#作为第一个字符，将任何记录标记为注释，解析器将忽略该注释。
