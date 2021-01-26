---
description: 对高级文本格式使用以下命令。
seo-description: 对高级文本格式使用以下命令。
seo-title: 高级文本格式
solution: Experience Manager
title: 高级文本格式
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
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
   <td> <p>以半分为准；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>上标，字体大小不变。 </p> </td> 
   <td> <p>以半分为准；默认值为6。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \字距 <span class="varname"> 调整N  </span> </span> </td> 
   <td> <p>以指定的字体大小禁用／启用。 </p> </td> 
   <td> <p>字体大小（以半点为单位），高于此值可应用字偶间距；0可禁用字距调整；对于所有字体大小在半点以上的字偶间距调整，默认值为1。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning optical  </span> </td> 
   <td> <p>选择视觉字距微调。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kernetric  </span> </td> 
   <td> <p>选择度量字距。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> n  </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正或负四分；默认值为0。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw  <span class="varname"> n  </span> </span> </td> 
   <td> <p>修改字符间距。 </p> </td> 
   <td> <p>正或负扭曲。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>水平字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>垂直字符缩放。 </p> </td> 
   <td> <p>正或负百分比；默认值为100;Dynamic Media分机。 </p> <p> <span class="codeph"> \charscaley </span> 在应用text=时也会缩放 <span class="codeph"> 行间距 </span>。<span class="codeph"> textPs=始 </span> 终保留行间距，而不管垂直字符缩放的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>选择从左到右字符流。 </p> </td> 
   <td> <p>默认. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>选择从右到左的字符流。 </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 仅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> n  </span> </span> </td> 
   <td> <p>启用复制调整并设置允许的最大字体大小。 </p> </td> 
   <td> <p>字体大小（半点）;<span class="codeph"> textPs= </span>;Dynamic Media分机。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> n  </span> </span> </td> 
   <td> <p>最大复制适合线（软限制）。 </p> </td> 
   <td> <p>0表示不限行；<span class="codeph"> textPs= </span>;Dynamic Media分机。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> n  </span> </span> </td> 
   <td> <p>最大复制适合线（截断）。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；Dynamic Media分机。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> n  </span> </span> </td> 
   <td> <p>字符方向。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限；对于非罗马字体被忽略；当\stextflow <span class="codeph"> 1不 </span> 起作用时忽略。 </p> <p>0垂直（默认）。 </p> <p>1顺时针旋转90度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

