---
description: 文本流排除区域。 指定要从文本流中排除的一个或多个区域。
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---

# textFlowXPath{#textflowxpath}

文本流排除区域。 指定要从文本流中排除的一个或多个区域。

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
</table>

有关其他信息，包括&#x200B;*`pathDefinition`*&#x200B;的说明，请参阅[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)。 如果未指定路径定义，则将忽略`textFlowXPath=`。

## 属性 {#section-cd1ebb151d4a405fbfc508d46522d686}

文本层属性（仅限`textPs=`）。 被其他层忽略，或者在未指定`textFlowPath=`时忽略。 如果为`layer=comp`指定，则应用于`layer=0`。

## 默认 {#section-9405cda904684d829ed12a9e40a4dc46}

无。

## 另请参阅 {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
