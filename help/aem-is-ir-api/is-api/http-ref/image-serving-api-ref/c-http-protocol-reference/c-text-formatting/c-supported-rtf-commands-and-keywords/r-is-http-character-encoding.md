---
description: 使用下列命令來編碼字元。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# 字元編碼{#character-encoding}

使用下列命令來編碼字元。

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
   <td> <span class="codeph">\`<span class="varname"> HH</span></span> </td> 
   <td> <p>單一8位元字元。 </p> </td> 
   <td> <p><span class="varname"> HH</span> 必須是2位數的十六進位值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>單一Unicode字元。 </p> </td> 
   <td> <p><span class="varname"> N</span> 是有正負號的2位元組整數，因此大於32767的Unicode值必須表示為負數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode字元大小。 </p> </td> 
   <td> <p>對應給定Unicode字元的位元組數。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>低ANSI區域的字元緊隨其後。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich </span> </td> 
   <td> <p>高ANSI區域的字元緊隨其後。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>後面跟著雙位元組字元。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
