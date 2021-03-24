---
description: 替换变量用于将值从请求URL传输到存储在服务器上的FXG模板。
solution: Experience Manager
title: 替换变量
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
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
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

* 变量定义和引用可能发生在请求URL的查询部分。
* 变量定义如上，与其他IS命令类似；前导“$”将命令标识为变量定义。
* 变量名`*`var`*`区分大小写，可能由字母、数字、“ — ”和“_”的任意组合组成。
* 重要值必须采用单次URL编码，才能进行安全HTTP传输。

