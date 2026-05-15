---
description: HTTP协议的基本语法如下。
solution: Experience Manager
title: 图像服务HTTP协议基本语法
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
TQID: 'https://experienceleague.adobe.com/fB60CyCuBYstiJJesDefrK1DW7w-2t0PJqqt-iLgZOA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# 图像服务HTTP协议基本语法{#image-serving-http-protocol-basic-syntax}

HTTP协议的基本语法如下：

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">请求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname">服务器</span>/is/image[/<span class="varname">对象</span>][？<span class="varname"> 修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">服务器</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">服务器地址</span>[：<span class="varname">端口</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">对象</span> </span> </p></td> 
  <td class="stentry"> <p>Source对象说明符（图像路径或图像目录条目）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">修饰符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">修饰符</span>*[&amp;<span class="varname">修饰符</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">修饰符</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">命令|{$<span class="varname">宏</span>$}|{.<span class="varname"> 评论</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">命令</span> </span> </p> </td> 
  <td class="stentry"> <p><code>{</code><span class="varname"> cmdName</span>|<code>{$</code><span class="varname">变量</span><code>}}[=</code><span class="varname">值</span><code>]</code> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">宏</span> </span> </p> </td> 
  <td class="stentry"> <p>命令宏的名称。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">评论</span> </span> </p></td> 
  <td class="stentry"> <p>注释字符串（被服务器忽略）。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>支持的命令或属性名称之一。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">变量</span> </span> </p> </td> 
  <td class="stentry"> <p>自定义变量的名称。</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span> </span> </p></td> 
  <td class="stentry"> <p>命令或变量值。 </p></td> 
 </tr> 
</table>

*`server_address`*、*`cmdName`*、*`macro`*&#x200B;和&#x200B;*`var`*&#x200B;不区分大小写。 服务器保留所有其他字符串值的大小写。

*`value`*&#x200B;是命令特定的，可以由一个或多个用逗号分隔的值组成。 有关详细信息，请参阅各个命令的描述。

## 服务器标识符 {#section-926ae55ddba14b8d952147a5fd701e14}

所有HTTP图像服务请求都需要[!DNL /is/image]根上下文。

## HTTP解码 {#section-20922baccd804d2d986b44ce9a183a7d}

图像服务首先从传入请求中提取&#x200B;*`object`*&#x200B;和&#x200B;*`modifiers`*。 然后将&#x200B;*`object`*&#x200B;分隔到单独进行HTTP解码的路径元素中。 *`modifiers`*&#x200B;字符串被分为&#x200B;*`command`*= *`value`*&#x200B;对，然后在命令特定的处理之前对&#x200B;*`value`*&#x200B;进行HTTP解码。

>[!NOTE]
>
>除非在文档中另有说明，否则所有不安全字符都必须按照HTTP标准进行编码。 有关详细信息，请参阅HTTP规范。

## 注释 {#section-69ef0be0f17a418c87a0eba21c2ddb00}

注释可以嵌入到任何位置的请求字符串中，并通过句点(.)进行标识 紧跟在命令分隔符(&amp;)之后。 该注释被下一个出现的（未编码的）命令分隔符终止。 此功能可用于向请求添加不供图像服务使用的信息，例如时间戳和数据库ID。

## 另请参阅 {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[数据类型](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa)，[HTTP/1.1规范](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
