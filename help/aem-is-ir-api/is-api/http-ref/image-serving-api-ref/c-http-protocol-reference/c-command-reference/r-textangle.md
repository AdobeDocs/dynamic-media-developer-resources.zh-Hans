---
description: 文本渲染方向。 指定用textPs=指定的文本排列并呈现到文本框（用size=或textFlowPath=定义）的角度。
solution: Experience Manager
title: textAngle
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# textAngle{#textangle}

文本渲染方向。 指定用textPs=指定的文本排列并呈现到文本框（用size=或textFlowPath=定义）的角度。

` textAngle= *`角度`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>方向角度（度）。 </p> </td> 
 </tr> 
</table>

正值将文本顺时针旋转；`textAngle=90`从上到下绘制文本。

## 属性 {#section-6d586a632daa4261a8ce62db56140b36}

图层属性。 适用于`layer=comp`时的`layer=0`。 如果未为此图层指定`textPs=`或指定`textPath=`，则忽略。

## 默认 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` 不旋转。

## 另请参阅 {#section-dccc29ff33704061b2519b56b7be45fd}

[Text Formatting](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [Text Positioning](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [textFlowPath](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)= [,  textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
