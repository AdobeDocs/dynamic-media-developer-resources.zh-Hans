---
description: 文本排列区域。 指定应将使用textPs=指定的文本排入的一个或多个区域。
seo-description: 文本排列区域。 指定应将使用textPs=指定的文本排入的一个或多个区域。
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# textFlowPath{#textflowpath}

文本排列区域。 指定应将使用textPs=指定的文本排入的一个或多个区域。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p> </td> 
 </tr> 
</table>

请参见[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)以了解其他信息，包括&#x200B;*`pathDefinition`*&#x200B;的说明。

当存在`textFlowPath=`时，将忽略RTF边距命令`\margl`、`\margr`、`\margt`和`\margb`。 如果未指定路径定义，则忽略`textFlowPath=`。

## 属性 {#section-b68dc887c6534ce8982cad740b3aeaa4}

文本图层属性（仅限`textPs=`）。 被其他图层忽略。 如果为`layer=comp`指定，则应用于`layer=0`。

## 默认 {#section-68c4559b9e8242059b82e5a39a455dfc}

与图层矩形相同；文本将填充整个图层矩形。

## 另请参阅 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15) [,文本图层](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
