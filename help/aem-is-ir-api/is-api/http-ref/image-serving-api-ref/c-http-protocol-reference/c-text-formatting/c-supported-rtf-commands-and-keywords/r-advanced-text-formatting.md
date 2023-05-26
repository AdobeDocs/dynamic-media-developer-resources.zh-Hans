---
description: 使用下列命令设置高级文本格式。
solution: Experience Manager
title: 高级文本格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# 高级文本格式{#advanced-text-formatting}

使用下列命令设置高级文本格式。

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 说明 </th> 
   <th class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>下标而不更改字体大小。 </p> </td> 
   <td> <p>位置为半点；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>上标而不更改字体大小。 </p> </td> 
   <td> <p>位置为半点；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字距微调 <span class="varname"> N </span> </span> </td> 
   <td> <p>禁用/启用指定字体大小。 </p> </td> 
   <td> <p>字体大小（以半点为单位），超过该点将应用字距微调；0表示禁用字距微调；默认值为1，表示对超过1/2点的所有字体大小进行字距微调。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>选择光学字距微调。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅此而已。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>选择量度字距微调。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正或负的四分之一点；默认值为0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正的或负的twips。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>水平字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>垂直字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100；Dynamic Media扩展。 </p> <p> <span class="codeph"> \charscaley </span> 应用时还可以缩放行距 <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> 无论垂直字符缩放量如何，始终保留行距。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>选择从左至右的字符流。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>选择从右至左的字符流。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 仅此而已。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \组排文字 <span class="varname"> N </span> </span> </td> 
   <td> <p>启用复制管接头并设置允许的最大字体大小。 </p> </td> 
   <td> <p>以半点为单位的字体大小； <span class="codeph"> textPs= </span> 仅限；Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \复制管线 <span class="varname"> N </span> </span> </td> 
   <td> <p>最大复制配合线（软限制）。 </p> </td> 
   <td> <p>0表示无行限制； <span class="codeph"> textPs= </span> 仅限；Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>最大复制适应行数（截断）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>字符方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；对于非罗马字体，忽略；当 <span class="codeph"> \stextflow1 </span> 并未生效。 </p> <p>0垂直（默认）。 </p> <p>1顺时针旋转90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
