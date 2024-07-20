---
title: 需要
description: 请求类型。 指定请求的类型。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# 需要{#req}

请求类型。 指定请求的类型。

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
   <td colname="col1"> <p> <span class="codeph">验证</span> </p> </td> 
   <td colname="col2"> <p> 返回使用提供的url修饰符渲染fxg时产生的任何错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">内容</span> </p> </td> 
   <td colname="col2"> <p> 返回包含<span class="codeph"> s7：element</span>属性值的所有元素的xml列表以及fxg文档中所有页面的列表。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>返回其<span class="codeph"> &lt;RichText/&gt;</span>元素溢出的XML列表。 </p> <p>返回在客户端处理时溢流的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素的XML列表。 只返回<span class="+ topic/ph pr-d/codeph codeph">个溢流的&lt;RichText/&gt;</span>元素。 使用<span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>时，<span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span>是必需的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>属性。 未列出任何不带<span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span>的溢出<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 列表中的每个<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素都具有<span class="+ topic/ph pr-d/codeph codeph"> s7：elementid</span>、<span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span>和溢流文本框架的定界框。 <span class="+ topic/ph pr-d/codeph codeph"> s7：endCharIndex</span>属性指示文章中的文本索引，文本可以容纳到框架中。 <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span>仅适用于所请求FXG中的<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 它不会列出任何嵌入式FXG中的任何<span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">已存在</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[，text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId唯一请求标识符 </p> <p>它返回名为catalogRecord.exists的单个属性。 如果图像或默认目录中存在指定的目录条目，则属性值设置为“1”，否则属性值设置为“0”。 针对/is/content上下文的req=exists请求指示静态内容目录中存在或不存在指定记录。 </p> </td> 
  </tr> 
 </tbody> 
</table>
