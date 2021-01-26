---
description: 支持以下段落格式设置命令。
seo-description: 支持以下段落格式设置命令。
seo-title: 段落格式
solution: Experience Manager
title: 段落格式
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 1%

---


# 段落格式{#paragraph-formatting}

支持以下段落格式设置命令。

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>将段落格式重置为默认值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>左对齐文本。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>右对齐文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>将文本水平居中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>水平对齐文本。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>左对齐段落的最后一行。 </p> </td> 
   <td> <p>默认；<span class="codeph"> textPs= </span>;如果<span class="codeph"> \qj </span>不活动，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>右对齐两端对齐的段落的最后一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；如果\qj <span class="codeph"> 不 </span> 处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>将两端对齐的段落的最后一行居中。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；如果\qj <span class="codeph"> 不 </span>处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>对两端对齐的段落的最后一行进行标记（延伸）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；如果\qj <span class="codeph"> 不 </span>处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>首行缩进。 </p> </td> 
   <td> <p>扭曲；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左缩进。 </p> </td> 
   <td> <p>扭曲；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右缩进。 </p> </td> 
   <td> <p>扭曲；仅<span class="codeph"> textPs= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行间间距。 </p> </td> 
   <td> <p>0（默认）用于自动行间距；正值仅在大于默认行间距时使用值；为负值以强制间距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> n  </span> </span> </td> 
   <td> <p>行间距多个标志。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>为twips，则设置为0（默认）；如果<span class="codeph"> \sl </span>是默认间距的倍数，则设置为1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段前有额外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>将<span class="codeph"> \sb </span>应用于文本框中的第一个段落，<span class="codeph"> textPs= </span>不应用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段后有额外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>将<span class="codeph"> \sa </span>应用于文本框中的最后一个段落，<span class="codeph"> textPs= </span>则不适用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

