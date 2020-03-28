---
description: 本节介绍Scene7图像渲染HTTP协议的基本语法。
seo-description: 本节介绍Scene7图像渲染HTTP协议的基本语法。
seo-title: 图像渲染HTTP协议基本语法
solution: Experience Manager
title: 图像渲染HTTP协议基本语法
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像渲染HTTP协议基本语法{#image-rendering-http-protocol-basic-syntax}

本节介绍Scene7图像渲染HTTP协议的基本语法。

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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/暗角<span class="varname"></span> ] [ ?<span class="varname"> 修改程序</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 伺服器 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 暗角 </span> </p> </td> 
   <td colname="col2"> <p>暗角说明符（相对文件路径或暗角目录条目）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 修改程序 </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; modifier <span class="varname"></span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> 命令</span> | { $ <span class="varname"> macro</span> $ }| { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 命令 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 宏 </span> </p> </td> 
   <td colname="col2"> <p>命令宏的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> 评论 </span> </p> </td> 
   <td colname="col2"> <p>注释字符串（服务器忽略）。 </p> </td> 
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

*`server`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不区分大小写。 服务器保留所有其他字符串值的大小写。

**服务器标识符**

对于向图 `/ir/render`像渲染发出的所有HTTP请求，“”根上下文是必需的。

**注释**

注释可以嵌入到任意位置的请求字符串中，并由句点(.)标识紧接在命令分隔符(&amp;)之后。 注释以（未编码）命令分隔符的下一个出现结束。 此功能可用于向非图像服务使用的请求添加信息，例如时间戳、数据库ID等。

**HTTP解码**

图像渲染首先从传 *`object`* 入的请 *`modifiers`* 求中提取和提取。 *`object`* 然后，将其分离为单独HTTP解码的路径元素。 该 *`modifiers`* 字符串分为 *`command`*=对 *`value`* ，然后在命令特定的处理 *`value`* 之前进行HTTP解码。
