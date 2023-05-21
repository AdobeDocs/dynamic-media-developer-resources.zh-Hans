---
description: 文字排文區域。 指定一或多個區域，以textPs=指定的文字應排入這些區域。
solution: Experience Manager
title: 文字流程路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 文字流程路徑{#textflowpath}

文字排文區域。 指定一或多個區域，以textPs=指定的文字應排入這些區域。

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p> </td> 
 </tr> 
</table>

另請參閱 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 以取得其他資訊，包括 *`pathDefinition`*.

RTF邊界指令 `\margl`， `\margr`， `\margt`、和 `\margb` 被忽略，當 `textFlowPath=` 存在。 如果未指定路徑定義， `textFlowPath=` 會忽略。

## 屬性 {#section-b68dc887c6534ce8982cad740b3aeaa4}

文字圖層屬性( `textPs=` 僅限)。 被其他圖層忽略。 套用至 `layer=0` 若指定給 `layer=comp`.

## 默认 {#section-68c4559b9e8242059b82e5a39a455dfc}

與圖層矩形相同；文字會填滿整個圖層矩形。

## 另请参阅 {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)， [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)， [文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
