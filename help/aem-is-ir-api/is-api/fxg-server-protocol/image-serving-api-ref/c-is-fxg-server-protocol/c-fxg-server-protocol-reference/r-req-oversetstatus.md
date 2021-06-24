---
description: 請求類型. 指定请求的类型。
solution: Experience Manager
title: 请求
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 3%

---

# 请求{#req}

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
   <td colname="col2"> <p> 返回使用提供的url修饰符渲染fxg时出现的任何错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内容</span> </p> </td> 
   <td colname="col2"> <p> 返回具有<span class="codeph"> s7:element</span>属性值的所有元素的xml列表以及fxg文档中所有页面的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>返回XML列表，其中<span class="codeph"> &lt;RichText/&gt;</span>元素被覆盖。 </p> <p>返回一个<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素的xml列表，这些元素在客户端进行处理时被覆盖。 将只返回超集的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> 使用req=oversetstatus <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 时， <span class="+ topic/ph pr-d/codeph codeph"> elementidis为必需属性</span>。未列出任何没有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>的覆盖集<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 列表中的每个<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素都具有<span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>和超集文本框架的边框。 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>属性指示文章中文本在框架中能够容纳到的文本索引。 <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusus仅适用于 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 请求的FXG中的元素。它不会列出任何嵌入式FXG中的任何<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一请求标识符 </p> <p>返回名为catalogRecord.exists的单个属性。 如果指定的目录条目存在于图像或默认目录中，则属性值将设置为“1”，否则，该属性值将设置为“0”。 针对/is/content上下文的req=exists请求将指示静态内容目录中是否存在指定的记录。 </p> </td> 
  </tr> 
 </tbody> 
</table>
