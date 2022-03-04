---
title: 图像渲染HTTP协议基本语法
description: 本节介绍Dynamic Media图像渲染HTTP协议的基本语法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---

# 图像渲染HTTP协议基本语法{#image-rendering-http-protocol-basic-syntax}

本节介绍Dynamic Media图像渲染HTTP协议的基本语法。

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>商品 </p> </th> 
   <th colname="col2" class="entry"> <p>定义 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 請求</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> 服务器</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> 修改程序</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> 端口</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette </span> </p> </td> 
   <td colname="col2"> <p>晕影说明符（相对文件路径或晕影目录条目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修改程序 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 修饰符</span> *[和 <span class="varname"> 修饰符</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 命令</span> | { $ <span class="varname"> 宏</span> $ } | { 。<span class="varname"> 评论</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> 值</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏 </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 评论 </span> </p> </td> 
   <td colname="col2"> <p>注释字符串（被服务器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>命令或属性的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>自定义变量的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 值 </span> </p> </td> 
   <td colname="col2"> <p>命令或变量值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*&#x200B;和 *`var`* 不区分大小写。 服务器将保留所有其他字符串值的大小写。

**服务器标识符**

&#39; `/ir/render`对于对图像渲染的所有HTTP请求，都需要根上下文。

**注释**

注释可以嵌入到任何位置的请求字符串中，并由句点(.)标识 紧跟命令分隔符(&amp;)。 注释以下次出现（未编码）命令分隔符时终止。 此功能可用于向不用于图像提供的请求添加信息，如时间戳和数据库ID。

**HTTP解码**

图像渲染首先提取 *`object`* 和 *`modifiers`* 从传入的请求。 的 *`object`* 然后，被分隔为单独HTTP解码的路径元素。 的 *`modifiers`* 字符串分隔为 *`command`*= *`value`* 对，和 *`value`* 然后，在命令特定处理之前进行HTTP解码。
