---
description: 替换变量用于将值从请求URL传输到存储在服务器上的FXG模板。
solution: Experience Manager
title: 替换变量
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# 替换变量{#substitution-variables}

替换变量用于将值从请求URL传输到存储在服务器上的FXG模板。

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>变量要设置到的值（字符串）。 </p> </td> 
 </tr> 
</table>

* 变量定义和引用可能发生在请求URL的查询部分中。
* 变量的定义如上所示，与其他IS命令类似；前导“$”将命令标识为变量定义。
* 变量名称`*`var`*`区分大小写，可以由字母、数字、“ — ”和“_”的任意组合组成。
* 重要值必须为单次传递URL编码，才能进行安全HTTP传输。
