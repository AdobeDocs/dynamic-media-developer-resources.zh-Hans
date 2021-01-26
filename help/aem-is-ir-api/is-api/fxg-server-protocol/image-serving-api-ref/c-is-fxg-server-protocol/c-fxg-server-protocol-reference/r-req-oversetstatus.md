---
description: 請求類型. 指定请求的类型。
seo-description: 請求類型. 指定请求的类型。
seo-title: req
solution: Experience Manager
title: req
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

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
   <td colname="col2"> <p> 返回使用提供的url修饰符呈现fxg时的任何错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> 返回所有元素的xml列表，其属性值为<span class="codeph"> s7:element</span>，在fxg文档中返回所有页的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 溢流状态</span> </p> </td> 
   <td colname="col2"> <p>返回XML列表，其中<span class="codeph"> &lt;RichText/&gt;</span>元素已溢流。 </p> <p>返回<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素的xml列表，这些元素在客户端进行溢流处理。 将只返回溢流的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 <span class="+ topic/ph pr-d/codeph codeph"> 使用req=oversetstatus</span> 时，s7: <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementidis是必 <span class="+ topic/ph pr-d/codeph codeph"> 需的属性</span>。未列出任何没有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>的溢流<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 列表中的每个<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素都具有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>和溢流文本框架的边框。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>属性指示文章中文本在框架中能够适应的文本索引。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 仅适用于所 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 请求FXG中的元素。它不会列表任何嵌入的FXG中的任何<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一请求标识符 </p> <p>返回名为catalogRecord.exists的单个属性。 如果图像或默认目录中存在指定的目录条目，则属性值将设置为“1”，否则，它将设置为“0”。 req=exists对/is/content上下文的请求将指示静态内容目录中是否存在指定记录。 </p> </td> 
  </tr> 
 </tbody> 
</table>

