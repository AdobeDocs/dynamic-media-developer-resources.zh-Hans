---
description: 支持以下段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# 段落格式{#paragraph-formatting}

支持以下段落格式命令。

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>命令 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>将段落格式重置为默认设置。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>左对齐文本。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>文本右对齐。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>水平居中对齐文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>水平对齐文本。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>左对齐段落的最后一行。 </p> </td> 
   <td> <p>默认； <span class="codeph"> textPs= </span> 仅限；忽略条件 <span class="codeph"> \qj </span>未处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>右对齐两端对齐的段落的最后一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；忽略条件 <span class="codeph"> \qj </span> 未处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>将两端对齐的段落的最后一行居中。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；忽略条件 <span class="codeph"> \qj </span>未处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>将（拉伸）两端对齐段落的最后一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；忽略条件 <span class="codeph"> \qj </span>未处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>第一行缩进。 </p> </td> 
   <td> <p>崔普斯； <span class="codeph"> textPs= </span> 仅此而已。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左缩进。 </p> </td> 
   <td> <p>崔普斯； <span class="codeph"> textPs= </span> 仅此而已。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右缩进。 </p> </td> 
   <td> <p>崔普斯； <span class="codeph"> textPs= </span> 仅此而已。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行间距。 </p> </td> 
   <td> <p>0（默认）表示自动行距；正值表示仅在大于默认行距时使用值；负值表示强制行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行距多个标志。 </p> </td> 
   <td> <p>设置为0（默认），如果 <span class="codeph"> \sl </span> 以双星为单位表示，如果为，则为1 <span class="codeph"> \sl </span> 为缺省间距的倍数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落前有多余的空格。 </p> </td> 
   <td> <p>崔普斯； <span class="codeph"> text= </span>应用 <span class="codeph"> \sb </span> 到文本框的第一段， <span class="codeph"> textPs= </span> 不会。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落后加空格。 </p> </td> 
   <td> <p>崔普斯； <span class="codeph"> text= </span> 应用 <span class="codeph"> \sa </span> 到文本框的最后一个段落， <span class="codeph"> textPs= </span> 不会。 </p> </td> 
  </tr> 
 </tbody> 
</table>
