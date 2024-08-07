---
title: 文本路径
description: 文本路径。 指定用作随textPs=一起提供的文本的基线的路径。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# 文本路径{#textpath}

文本路径。 指定用作随textPs=一起提供的文本的基线的路径。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
</table>

请参阅[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以获取其他信息，包括&#x200B;*`pathDefinition`*&#x200B;的说明。

>[!NOTE]
>
>与`clipPath=`不同，当子路径的末尾未指定“z”或“Z”时，文本路径不会自动关闭。

*`pathDefinition`*&#x200B;可能包含多个子路径。 文本将按照指定的顺序在子路径上呈现。

RTF命令`\ql`、`\qc`、`\qr`、`\li`和`\ri`可用于沿路径定位渲染的文本。

## 属性 {#section-068137df436c46b9b55d271eb60e7285}

文本图层属性（仅限`textPs=`）。 被其他层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。 如果`textPs=`存在，则忽略。

如果层同时包括`textPath=`和`textFlowPath=`，则返回错误。

## 默认 {#section-697b1f2cfc43498080a31327e6eb173d}

无，用于标准文本渲染。

## 另请参阅 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ，[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)，[textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)，[文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
