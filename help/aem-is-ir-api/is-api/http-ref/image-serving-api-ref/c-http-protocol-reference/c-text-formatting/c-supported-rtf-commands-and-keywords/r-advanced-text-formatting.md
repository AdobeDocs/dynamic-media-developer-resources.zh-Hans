---
description: 对高级文本格式使用以下命令。
solution: Experience Manager
title: 高级文本格式
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---

# 高级文本格式{#advanced-text-formatting}

对高级文本格式使用以下命令。

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
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>下标时字体大小不会更改。 </p> </td> 
   <td> <p>半分；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>上标，不更改字体大小。 </p> </td> 
   <td> <p>半分；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字 <span class="varname"> 距N  </span> </span> </td> 
   <td> <p>在指定的字体大小处禁用/启用。 </p> </td> 
   <td> <p>以半点表示的字体大小，在上方应用字距微调；0禁用字距调整；对于在1/2点以上对所有字体大小进行字距微调，默认值为1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernotical  </span> </td> 
   <td> <p>选择光学字距调整。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernetric  </span> </td> 
   <td> <p>选择量度字距调整。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正或负四分；默认值为0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expntw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正扭曲或负扭曲。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>水平字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>垂直字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100;Dynamic Media扩展。 </p> <p> <span class="codeph"> \charscaley在 </span> 应用text=时还会缩放行 <span class="codeph"> 距 </span>。<span class="codeph"> textPs=始 </span> 终保留行间距，而不考虑垂直字符缩放的量。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>选择从左到右的字符流。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>选择从右到左的字符流。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 仅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>启用复制拟合并设置允许的最大字体大小。 </p> </td> 
   <td> <p>字体大小（以半点为单位）；仅<span class="codeph"> textPs= </span>;Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大副本拟合行数（软限制）。 </p> </td> 
   <td> <p>0表示不限行；仅<span class="codeph"> textPs= </span>;Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>最大副本拟合行数（截断）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>字符方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;对于非罗马字体被忽略；当\stextflow <span class="codeph"> 1未生 </span> 效时忽略。 </p> <p>0垂直（默认）。 </p> <p>1顺时针旋转90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>
