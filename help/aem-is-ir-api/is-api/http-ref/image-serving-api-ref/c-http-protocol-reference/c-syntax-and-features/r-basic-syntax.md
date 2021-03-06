---
description: HTTP协议的基本语法如下所示。
solution: Experience Manager
title: 图像服务HTTP协议基本语法
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# 图像服务HTTP协议基本语法{#image-serving-http-protocol-basic-syntax}

HTTP协议的基本语法如下：

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 请求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 服务器  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 对象</span> </span> </p></td> 
  <td class="stentry"> <p>源对象说明符（图像路径或图像目录条目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰语</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰符</span>*[&amp;<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname"> macro</span>$}|{。<span class="varname"> 注释</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname">值</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名称。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 评论</span> </span> </p></td> 
  <td class="stentry"> <p>注释字符串（被服务器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>支持的命令或属性名称之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>自定义变量的名称。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span> </span> </p></td> 
  <td class="stentry"> <p>命令或变量值。 </p></td> 
 </tr> 
</table>

*`server_address`*、  *`cmdName`*、 *`macro`*&#x200B;和 *`var`* 不区分大小写。服务器将保留所有其他字符串值的大小写。

*`value`* 是特定于命令的，可由一个或多个值组成，并用逗号分隔。有关详细信息，请参阅各个命令的说明。

## 服务器标识符 {#section-926ae55ddba14b8d952147a5fd701e14}

所有对图像服务的HTTP请求都需要[!DNL /is/image]根上下文。

## HTTP解码 {#section-20922baccd804d2d986b44ce9a183a7d}

图像服务首先从传入请求中提取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 *`object`* 然后，被分隔为单独HTTP解码的路径元素。将&#x200B;*`modifiers`*&#x200B;字符串分隔为&#x200B;*`command`*= *`value`*&#x200B;对，然后在命令特定处理之前对&#x200B;*`value`*&#x200B;进行HTTP解码。

>[!NOTE]
>
>除非文档另有说明，否则必须按照HTTP标准对所有不安全字符进行编码。 有关详细信息，请参阅HTTP规范。

## 注释 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注释可以嵌入到任意位置的请求字符串中，并由句点(.)标识 紧跟命令分隔符(&amp;)。 注释以下次出现（未编码）命令分隔符时终止。 此功能可用于向不用于图像提供的请求添加信息，如时间戳和数据库ID。

## 另请参阅 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[数据类型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)、 [HTTP/1.1规范](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
