---
description: 文本框中支持以下文档属性。
seo-description: 文本框中支持以下文档属性。
seo-title: 文档（文本框）属性
solution: Experience Manager
title: 文档（文本框）属性
topic: Scene7 Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 文档（文本框）属性{#document-text-box-properties}

文本框中支持以下文档属性。

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
   <td> <span class="codeph"> \fontbl </span> </td> 
   <td> <p>字体表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span></span> </td> 
   <td> <p>字体 <i>N的字符集</i>。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGB颜色表。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK颜色表。 </p> </td> 
   <td> <p>Scene7扩展。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>图像服务颜色的颜色表。 </p> </td> 
   <td> <p>Scene7扩展；文 <span class="codeph"> 本Ps=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span></span> </td> 
   <td> <p>红色组件。 </p> </td> 
   <td> <p>只能出现在 <span class="codeph"> \colortbl中 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span></span> </td> 
   <td> <p>绿色组件。 </p> </td> 
   <td> <p>只能出现在 <span class="codeph"> \colortbl中 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span></span> </td> 
   <td> <p>蓝色组件。 </p> </td> 
   <td> <p>只能出现在 <span class="codeph"> \colortbl中 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span></span> </td> 
   <td> <p>青色组件。 </p> </td> 
   <td> <p>Scene7扩展；只能出现在 <span class="codeph"> \cmykcolortbl中 </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span></span> </td> 
   <td> <p>洋红色组件。 </p> </td> 
   <td> <p>Scene7扩展；只能出现在 <span class="codeph"> \cmykcolortbl中 </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span></span> </td> 
   <td> <p>黄色组件。 </p> </td> 
   <td> <p>Scene7扩展；只能出现在 <span class="codeph"> \cmykcolortbl中 </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span></span> </td> 
   <td> <p>黑色组件。 </p> </td> 
   <td> <p>Scene7扩展；只能出现在 <span class="codeph"> \cmykcolortbl中 </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span></span> </td> 
   <td> <p>左边距。 </p> </td> 
   <td> <p>Twips;文 <span class="codeph"> 本Ps=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span></span> </td> 
   <td> <p>右边距。 </p> </td> 
   <td> <p>Twips;文 <span class="codeph"> 本Ps=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span></span> </td> 
   <td> <p>上边距。 </p> </td> 
   <td> <p>Twips;文 <span class="codeph"> 本Ps=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span></span> </td> 
   <td> <p>底部边距。 </p> </td> 
   <td> <p>Twips;文 <span class="codeph"> 本Ps=仅 </span> 限 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>文本框中的顶对齐文本。 </p> </td> 
   <td> <p>默认 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>文本框中的底对齐文本。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>将文本居中。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span></span> </td> 
   <td> <p>文本排列方向。 </p> </td> 
   <td> <p>特定于语言的文本流；文 <span class="codeph"> 本Ps= </span> 仅0（默认）左右，上下（欧洲）1从上到下，左右（远东） </p> </td> 
  </tr> 
 </tbody> 
</table>

