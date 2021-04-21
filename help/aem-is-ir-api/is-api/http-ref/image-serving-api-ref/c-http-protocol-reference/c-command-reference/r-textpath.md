---
description: 文本路径。 指定用作随textPs=提供的文本的基线的路径。
solution: Experience Manager
title: textPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---


# textPath{#textpath}

文本路径。 指定用作随textPs=提供的文本的基线的路径。

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
</table>

请参见[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以了解其他信息，包括&#x200B;*`pathDefinition`*&#x200B;的说明。

>[!NOTE]
>
>与`clipPath=`不同，当子路径末尾未指定“z”或“Z”时，文本路径不会自动关闭。

*`pathDefinition`* 可能包括多个子路径。文本按指定顺序呈现在子路径上。

RTF命令`\ql`、`\qc`、`\qr`、`\li`和`\ri`可用于沿路径放置渲染的文本。

## 属性 {#section-068137df436c46b9b55d271eb60e7285}

文本图层属性（仅限`textPs=`）。 被其他图层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。 如果存在`textPs=`，则忽略。

如果图层同时包含`textPath=`和`textFlowPath=`，则返回错误。

## 默认 {#section-697b1f2cfc43498080a31327e6eb173d}

无，用于标准文本渲染。

## 另请参阅 {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
