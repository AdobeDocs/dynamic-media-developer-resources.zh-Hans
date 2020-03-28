---
description: HTTP协议的基本语法如下所示。
seo-description: HTTP协议的基本语法如下所示。
seo-title: 图像服务HTTP协议基本语法
solution: Experience Manager
title: 图像服务HTTP协议基本语法
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像服务HTTP协议基本语法{#image-serving-http-protocol-basic-syntax}

HTTP协议的基本语法如下所示。

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 请 <span class="varname"> 求</span></span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 服务器 </span></span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 对 <span class="varname"> 象</span></span> </p></td> 
  <td class="stentry"> <p>源对象说明符（图像路径或图像目录条目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 修 <span class="varname"> 饰符</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 修 <span class="varname"> 饰符</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 修 <span class="varname"> 饰符</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span></span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span></span> </p> </td> 
  <td class="stentry"> <p>命令宏的名称。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 注 <span class="varname"> 释</span></span> </p></td> 
  <td class="stentry"> <p>注释字符串（服务器忽略）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span></span> </p></td> 
  <td class="stentry"> <p>支持的命令或属性名称之一。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span></span> </p> </td> 
  <td class="stentry"> <p>自定义变量的名称。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span></span> </p></td> 
  <td class="stentry"> <p>命令或变量值。 </p></td> 
 </tr> 
</table>

*`server_address`*、 *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不区分大小写。 服务器保留所有其他字符串值的大小写。

*`value`* 是命令特定的，可能由一个或多个值组成，这些值以逗号分隔。 有关详细信息，请参阅各个命令的说明。

## 服务器标识符 {#section-926ae55ddba14b8d952147a5fd701e14}

对图 [!DNL /is/image] 像服务的所有HTTP请求都需要根上下文。

## HTTP解码 {#section-20922baccd804d2d986b44ce9a183a7d}

图像服务首先从传入 *`object`* 的请 *`modifiers`* 求中提取和提取。 *`object`* 然后，将其分离为单独HTTP解码的路径元素。 该 *`modifiers`* 字符串分为 *`command`*=对 *`value`* ，然后在命令特定的处理 *`value`* 之前进行HTTP解码。

>[!NOTE]
>
>除非文档中另有说明，否则所有不安全字符必须按照HTTP标准进行编码。 有关详细信息，请参阅HTTP规范。

## 注释 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注释可以嵌入到任意位置的请求字符串中并由句点(.)标识紧接在命令separator(&amp;)之后。 注释以（未编码）命令分隔符的下一个出现结束。 此功能可用于向非图像服务使用的请求添加信息，例如时间戳、数据库ID等。

## 另请参阅 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[数据类型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1规范](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
