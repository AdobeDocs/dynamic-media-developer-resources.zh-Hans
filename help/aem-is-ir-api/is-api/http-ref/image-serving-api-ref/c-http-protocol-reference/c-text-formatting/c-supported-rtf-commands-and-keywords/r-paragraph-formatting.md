---
description: 支持以下段落格式命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
TQID: 'https://experienceleague.adobe.com/bksi7t36irm8XQqI0LtJl3kNaSCZANRzbCKf80o-eNM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

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
   <td> <p> 仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>左对齐文本。 </p> </td> 
   <td> <p>默认。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>右对齐文本。 </p> </td> 
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
   <td> <p> 仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>左对齐段落的最后一行。 </p> </td> 
   <td> <p>默认；仅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>右对齐对齐段落的最后一行。 </p> </td> 
   <td> <p> 仅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未处于活动状态，则忽略该项。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>将两端对齐的段落的最后一行置中。 </p> </td> 
   <td> <p> 仅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未处于活动状态，则忽略它。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>将（拉伸）两端对齐的段落的最后一行悬置。 </p> </td> 
   <td> <p> 仅<span class="codeph"> textPs= </span>；如果<span class="codeph"> \qj </span>未处于活动状态，则忽略它。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>首行缩进。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左缩进。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右缩进。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行间距。 </p> </td> 
   <td> <p>0（默认值）表示自动行距；正值表示仅在大于默认行距时使用值；负值表示强制行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行距多个标志。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>为twips格式，则设置为0（默认值）；如果<span class="codeph"> \sl </span>为默认间距的倍数，则设置为1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落前有多余的空格。 </p> </td> 
   <td> <p>Twips； <span class="codeph"> text= </span>将<span class="codeph"> \sb </span>应用于文本框中的第一段，<span class="codeph"> textPs= </span>不应用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落后加空格。 </p> </td> 
   <td> <p>Twips； <span class="codeph"> text= </span>将<span class="codeph"> \sa </span>应用于文本框中的最后一个段落，<span class="codeph"> textPs= </span>不应用。 </p> </td> 
  </tr> 
 </tbody> 
</table>
