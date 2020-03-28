---
description: 文本排除区域。 指定要从文本排列中排除的一个或多个区域。
seo-description: 文本排除区域。 指定要从文本排列中排除的一个或多个区域。
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textFlowXPath{#textflowxpath}

文本排除区域。 指定要从文本排列中排除的一个或多个区域。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
</table>

请参 [阅clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) ，以了解其他信息，包括对的说明 *`pathDefinition`*。 如果未指定路径定义，则 `textFlowXPath=` 忽略该定义。

## 属性 {#section-cd1ebb151d4a405fbfc508d46522d686}

文本图层属性( `textPs=` 仅限)。 被其他图层忽略，或者当指定时未指定 `textFlowPath=`。 如果为 `layer=0` 指定，则应用 `layer=comp`于。

## 默认 {#section-9405cda904684d829ed12a9e40a4dc46}

无。

## 另请参阅 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
