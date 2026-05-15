---
description: 替换变量用于将请求URL中的值传输到存储在服务器上的FXG模板。
solution: Experience Manager
title: 替代变量
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
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
