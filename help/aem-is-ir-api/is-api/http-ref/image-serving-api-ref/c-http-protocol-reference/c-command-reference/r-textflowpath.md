---
description: 文本流区域。 指定应将使用textPs=指定的文本流入的一个或多个区域。
solution: Experience Manager
title: textFlowPath
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# textFlowPath{#textflowpath}

文本流区域。 指定应将使用textPs=指定的文本流入的一个或多个区域。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p> </td> 
 </tr> 
</table>

有关其他信息，包括&#x200B;*`pathDefinition`*&#x200B;的说明，请参阅[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。

当存在`textFlowPath=`时，将忽略RTF边距命令`\margl`、`\margr`、`\margt`和`\margb`。 如果未指定路径定义，则将忽略`textFlowPath=`。

## 属性 {#section-b68dc887c6534ce8982cad740b3aeaa4}

文本层属性（仅限`textPs=`）。 被其他层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。

## 默认 {#section-68c4559b9e8242059b82e5a39a455dfc}

与层矩形相同；文本将填充整个图层矩形。

## 另请参阅 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15),  [文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
