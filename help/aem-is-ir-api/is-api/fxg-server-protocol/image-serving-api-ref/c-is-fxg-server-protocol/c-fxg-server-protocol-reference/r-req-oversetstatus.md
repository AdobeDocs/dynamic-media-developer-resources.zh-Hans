---
description: 請求類型. 指定请求的类型。
seo-description: 請求類型. 指定请求的类型。
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

請求類型. 指定请求的类型。

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 值 </th> 
   <th colname="col2" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 确认</span> </p> </td> 
   <td colname="col2"> <p> 返回使用提供的url修饰符呈现fxg时的所有错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> 返回所有元素的xml列表，其 <span class="codeph"></span> s7:element属性值和fxg文档中所有页面的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>返回其&lt;RichText/&gt;元 <span class="codeph"> 素溢流的XML列表</span> 。 </p> <p>返回&lt;RichText/&gt;元 <span class="+ topic/ph pr-d/codeph codeph"> 素的xml列表</span> ，这些元素在客户端进行溢流处理。 将 <span class="+ topic/ph pr-d/codeph codeph"> 只返回溢流的</span> &lt;RichText/&gt;元素。 <span class="+ topic/ph pr-d/codeph codeph"> 使用req=oversetstatus</span> 时，s7:elementid <span class="+ topic/ph pr-d/codeph codeph"> 是必需的&lt;RichText/&gt;</span> 属性 <span class="+ topic/ph pr-d/codeph codeph"></span>。 不列 <span class="+ topic/ph pr-d/codeph codeph"> 出任何没有s7:elementid</span> 的溢流 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;元素</span> 。 列表 <span class="+ topic/ph pr-d/codeph codeph"> 中的每个</span> &lt;RichText/&gt;元素都有 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>，以及溢流文本框架的边框。 s7: <span class="+ topic/ph pr-d/codeph codeph"> endCharIndex</span> 属性指示文章中文本在框架中能够适应到的文本索引。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 仅适用于所请 <span class="+ topic/ph pr-d/codeph codeph"> 求的FXG中的&lt;RichText/&gt;</span> elements。 它不会列表任 <span class="+ topic/ph pr-d/codeph codeph"> 何嵌入的FXG中的</span> &lt;RichText/&gt;元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一请求标识符 </p> <p>返回名为catalogRecord.exists的单个属性。 如果指定的目录条目存在于图像或默认目录中，则该属性值将设置为“1”，否则将设置为“0”。 req=exists对/is/content上下文的请求将指示静态内容目录中是否存在指定记录。 </p> </td> 
  </tr> 
 </tbody> 
</table>

