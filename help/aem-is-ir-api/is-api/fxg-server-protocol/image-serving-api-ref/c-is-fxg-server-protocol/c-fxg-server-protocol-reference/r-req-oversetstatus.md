---
title: 需要
description: 請求類型. 指定请求的类型。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# 需要{#req}

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
   <td colname="col2"> <p> 返回使用提供的url修饰符渲染fxg时产生的任何错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> 返回所有元素的xml列表，其中 <span class="codeph"> s7：element</span> 属性值和fxg文档中所有页面的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>返回的XML列表，其中 <span class="codeph"> &lt;richtext /&gt;</span> 元素溢出。 </p> <p>返回的xml列表 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素溢出，以便在客户端进行处理。 仅 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 返回溢出的元素。 此 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span> 是必需的 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 使用时的属性 <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. 任何溢出 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素没有 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span> 未列出。 每个 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 列表中的元素具有 <span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span>， <span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span>和溢流文本框架的边界框。 此 <span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span> 属性指示文章中的文本索引，文本可以容纳到框架中。 此 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 仅适用于 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 元素中包含的FXG。 它不会列出任何 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 任何嵌入的FXG中的元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[，text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一请求标识符 </p> <p>它返回名为catalogRecord.exists的单个属性。 如果图像或默认目录中存在指定的目录条目，则属性值设置为“1”，否则属性值设置为“0”。 针对/is/content上下文的req=exists请求指示静态内容目录中存在或不存在指定记录。 </p> </td> 
  </tr> 
 </tbody> 
</table>
