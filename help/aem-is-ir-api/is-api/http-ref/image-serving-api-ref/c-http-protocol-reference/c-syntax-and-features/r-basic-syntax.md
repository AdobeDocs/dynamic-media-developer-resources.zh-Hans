---
description: HTTP协议的基本语法如下。
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
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> 服务器</span>/is/image[/<span class="varname"> 对象</span>][？<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 服务器 </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[：<span class="varname"> 端口</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 对象</span> </span> </p></td> 
  <td class="stentry"> <p>源对象说明符（图像路径或图像目录条目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰符</span>*[&amp;<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 修饰符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname"> 宏</span>$}|{.<span class="varname"> 注释</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 命令</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> 值</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名称。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 注释</span> </span> </p></td> 
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

*`server_address`*， *`cmdName`*， *`macro`*、和 *`var`* 不区分大小写。 服务器保留所有其他字符串值的大小写。

*`value`* 是命令特定的，可以由一个或多个用逗号分隔的值组成。 有关详细信息，请参阅各个命令的说明。

## 服务器标识符 {#section-926ae55ddba14b8d952147a5fd701e14}

此 [!DNL /is/image] 所有HTTP图像服务请求都需要根上下文。

## HTTP解码 {#section-20922baccd804d2d986b44ce9a183a7d}

图像服务首次提取 *`object`* 和 *`modifiers`* 来自传入请求。 *`object`* 然后被分离成路径元素，这些元素被单独进行HTTP解码。 此 *`modifiers`* 字符串被分隔为 *`command`*= *`value`* 对，和 *`value`* 然后在命令特定的处理之前进行HTTP解码。

>[!NOTE]
>
>除非文档中另有说明，否则所有不安全字符都必须按照HTTP标准进行编码。 有关详细信息，请参阅HTTP规范。

## 注释 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注释可以嵌入到任何位置的请求字符串中，并以period(.)进行标识 紧跟在命令分隔符(&amp;)之后。 该注释由下一个出现的（未编码）命令分隔符终止。 此功能可用于向请求添加不适用于图像服务的信息，例如时间戳和数据库ID。

## 另请参阅 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[数据类型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)， [HTTP/1.1规范](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
