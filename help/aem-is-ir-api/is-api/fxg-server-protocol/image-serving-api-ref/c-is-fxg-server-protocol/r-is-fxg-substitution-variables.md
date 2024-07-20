---
description: 替换变量用于将请求URL中的值传输到存储在服务器上的FXG模板。
solution: Experience Manager
title: 替代变量
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# 替代变量{#substitution-variables}

替换变量用于将请求URL中的值传输到存储在服务器上的FXG模板。

` $ *`变量`*= *`值`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">变量</span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

* 变量定义和引用可能会出现在请求URL的查询部分中。
* 变量的定义如上所述，与其他IS命令类似；前导“$”将该命令标识为变量定义。
* 变量名称`*`var`*`区分大小写，并可由字母、数字、“ — ”和“_”的任意组合组成。
* 重要值必须为单通道URL编码，以便安全HTTP传输。
