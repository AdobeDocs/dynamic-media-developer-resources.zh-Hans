---
description: 支持以下段落格式设置命令。
solution: Experience Manager
title: 段落格式
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
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
   <td> <p> <span class="codeph"> textPs= </span> 仅限 </p> </td> 
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
   <td> <p>水平居中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>水平对齐文本。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>左对齐段落的最后一行。 </p> </td> 
   <td> <p>默认；<span class="codeph"> textPs= </span>;如果<span class="codeph"> \qj </span>不活动，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>右对齐两端对齐段落的最后一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果\ <span class="codeph"> qj不 </span> 处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>居中对齐段落的最后一行。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果\ <span class="codeph"> qj不 </span>处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>对两端对齐的段落的最后一行进行延伸。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;如果\ <span class="codeph"> qj不 </span>处于活动状态，则忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>首行缩进。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左缩进。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> n  </span> </span> </td> 
   <td> <p>右缩进。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行间间距。 </p> </td> 
   <td> <p>0（默认）用于自动行间距；值为正值时，仅在大于默认行间距时使用值；为负值以强制间距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> n  </span> </span> </td> 
   <td> <p>行间距多个标志。 </p> </td> 
   <td> <p>如果<span class="codeph"> \sl </span>为twip，则设置为0（默认）；如果<span class="codeph"> \sl </span>为默认间距的倍数，则设置为1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落前有额外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>将<span class="codeph"> \sb </span>应用于文本框中的第一个段落，<span class="codeph"> textPs= </span>则不应用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落后有额外空格。 </p> </td> 
   <td> <p>扭曲；<span class="codeph"> text= </span>将<span class="codeph"> \sa </span>应用于文本框中的最后一个段落，<span class="codeph"> textPs= </span>则不适用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

