---
description: 文本框支持以下文档属性。
solution: Experience Manager
title: 文档（文本框）属性
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# 文档（文本框）属性{#document-text-box-properties}

文本框支持以下文档属性。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fontbl  </span> </td> 
   <td> <p>字体表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f字符集 <span class="varname"> N  </span> </span> </td> 
   <td> <p>字体<i>N</i>的字符集。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colorbl  </span> </td> 
   <td> <p>RGB颜色表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>CMYK颜色表。 </p> </td> 
   <td> <p>Dynamic Media扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>图像服务颜色的颜色表。 </p> </td> 
   <td> <p>Dynamic Media扩展；<span class="codeph">文本Ps= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>红色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> n  </span> </span> </td> 
   <td> <p>绿色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> n  </span> </span> </td> 
   <td> <p>蓝色组件。 </p> </td> 
   <td> <p>只能出现在<span class="codeph"> \colortbl </span>中；0..255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \青 <span class="varname"> N  </span> </span> </td> 
   <td> <p>青色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \洋红色 <span class="varname"> N  </span> </span> </td> 
   <td> <p>洋红色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黄 <span class="varname"> N  </span> </span> </td> 
   <td> <p>黄色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> n  </span> </span> </td> 
   <td> <p>黑色组件。 </p> </td> 
   <td> <p>Dynamic Media扩展；只能出现在<span class="codeph"> \cmykcolortbl </span>中；0..100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> n  </span> </span> </td> 
   <td> <p>左边距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \marg  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右边距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> n  </span> </span> </td> 
   <td> <p>上边距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> n  </span> </span> </td> 
   <td> <p>下边距。 </p> </td> 
   <td> <p>扭曲；<span class="codeph">文本Ps= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vert  </span> </td> 
   <td> <p>文本框中的顶对齐文本。 </p> </td> 
   <td> <p>默认 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \版本  </span> </td> 
   <td> <p>文本框中的底对齐文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>将文本居中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> n  </span> </span> </td> 
   <td> <p>文本排列方向。 </p> </td> 
   <td> <p>特定语言的文本流；<span class="codeph"> textPs= </span>仅0（默认）左右、上下（欧洲）1从上到下、左右（远东） </p> </td> 
  </tr> 
 </tbody> 
</table>

