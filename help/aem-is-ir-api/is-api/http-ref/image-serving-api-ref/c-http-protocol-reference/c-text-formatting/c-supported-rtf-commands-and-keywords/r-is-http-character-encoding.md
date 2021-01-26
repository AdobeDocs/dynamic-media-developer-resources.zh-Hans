---
description: 使用以下命令对字符进行编码。
seo-description: 使用以下命令对字符进行编码。
seo-title: 字符编码
solution: Experience Manager
title: 字符编码
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7b19b831-b40c-4f26-83a4-732c578dbbf0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---


# 字符编码{#character-encoding}

使用以下命令对字符进行编码。

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 说明 </th> 
   <th class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>单个8位字符。 </p> </td> 
   <td> <p><span class="varname"> 该</span> 值必须是2位数的十六进制值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>单个Unicode字符。 </p> </td> 
   <td> <p><span class="varname"> Nis</span> 是带符号的2字节整数，因此大于32767的Unicode值必须表示为负数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode字符大小。 </p> </td> 
   <td> <p>与给定的Unicode字符对应的字节数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>下面是低ANSI区域的字符。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hc  </span> </td> 
   <td> <p>高ANSI区域的字符后面是。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>多次字节字符后面是。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

