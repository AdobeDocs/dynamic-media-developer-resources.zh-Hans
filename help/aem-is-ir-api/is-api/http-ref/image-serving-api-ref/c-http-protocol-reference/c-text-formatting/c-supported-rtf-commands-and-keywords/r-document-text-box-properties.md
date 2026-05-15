---
description: 文本框支持以下文档属性。
solution: Experience Manager
title: 文档（文本框）属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
TQID: 'https://experienceleague.adobe.com/U8T6F0KmGyopf6rXM0-zssY-hpfKPVUHWt-vO8aA7xM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 文档（文本框）属性{#document-text-box-properties}

文本框支持以下文档属性。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
   <th class="entry"> <b>备注</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>字型表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>字体<i>N</i>的字符集。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGB色表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK颜色表。 </p> </td> 
   <td> <p>Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>图像提供颜色的颜色表。 </p> </td> 
   <td> <p>Dynamic Media扩展；仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>红色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>； 0...255中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>绿色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>； 0...255中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>蓝色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>； 0...255中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>青色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>； 0...100中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>洋红色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>； 0...100中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黄色<span class="varname"> N </span> </span> </td> 
   <td> <p>黄色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>； 0...100中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>黑色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>； 0...100中 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>左边距。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>右边距。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>上边距。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>下边距。 </p> </td> 
   <td> <p>Twips；仅<span class="codeph"> textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>文本框中的顶对齐文本。 </p> </td> 
   <td> <p>默认 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>文本框中的下对齐文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>文本框中的文本居中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>文本流方向。 </p> </td> 
   <td> <p>特定语言的文本流；<span class="codeph"> textPs= </span>仅0（默认）左右、上下（欧洲） 1上下、右左（远东） </p> </td> 
  </tr> 
 </tbody> 
</table>
