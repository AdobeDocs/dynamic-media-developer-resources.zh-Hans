---
description: 本节介绍Dynamic Media图像渲染HTTP协议的基本语法。
seo-description: 本节介绍Dynamic Media图像渲染HTTP协议的基本语法。
seo-title: 图像渲染HTTP协议基本语法
solution: Experience Manager
title: 图像渲染HTTP协议基本语法
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname">暗角</span> ] [ ?<span class="varname"> 修改程序</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 暗角  </span> </p> </td> 
   <td colname="col2"> <p>暗角说明符（相对文件路径或暗角目录条目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修改程序 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp;  <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $  <span class="varname"> macro</span> $ } | {<span class="varname"> 注释</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏  </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 评论  </span> </p> </td> 
   <td colname="col2"> <p>注释字符串（服务器忽略）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>命令或属性的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>自定义变量的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 值  </span> </p> </td> 
   <td colname="col2"> <p>命令或变量值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不区分大小写。服务器保留所有其他字符串值的大小写。

**服务器标识符**

对于向图像渲染发出的所有HTTP请求，“ `/ir/render`”根上下文是必需的。

**注释**

注释可以嵌入到任意位置的请求字符串中，并由句点(.)标识 紧接在命令分隔符(&amp;)之后。 注释以下次出现（未编码）命令分隔符结束。 此功能可用于向不用于图像服务的请求添加信息，如时间戳、数据库id等。

**HTTP解码**

图像渲染首先从传入请求中提取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然后，将其分离为路径元素，这些元素将单独HTTP解码。将&#x200B;*`modifiers`*&#x200B;字符串分为&#x200B;*`command`*= *`value`*&#x200B;对，然后在命令特定处理之前对&#x200B;*`value`*&#x200B;进行HTTP解码。
