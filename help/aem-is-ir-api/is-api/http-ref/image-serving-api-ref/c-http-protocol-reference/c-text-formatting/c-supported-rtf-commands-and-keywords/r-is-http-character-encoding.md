---
title: 字符编码
description: 使用以下命令对字符进行编码。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '88'
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
   <td> <p><span class="varname"> HH</span>必须为2位数的十六进制值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>单个Unicode字符。 </p> </td> 
   <td> <p><span class="varname"> N</span>是带符号的2字节整数，因此大于32767的Unicode值必须表示为负数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode字符大小。 </p> </td> 
   <td> <p>与给定Unicode字符对应的字节数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>字符来自低ANSI区域。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>字符来自高ANSI区域。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>后面是双字节字符。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
