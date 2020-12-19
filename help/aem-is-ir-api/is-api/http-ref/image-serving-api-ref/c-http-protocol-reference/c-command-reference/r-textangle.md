---
description: 文本渲染方向。 指定用textPs=指定的文本排版并呈现到文本框中的角度（用size=或textFlowPath=定义）。
seo-description: 文本渲染方向。 指定用textPs=指定的文本排版并呈现到文本框中的角度（用size=或textFlowPath=定义）。
seo-title: textAngle
solution: Experience Manager
title: textAngle
topic: Scene7 Image Serving - Image Rendering API
uuid: ac54c186-1fc5-479a-89f2-ff2da5e7999a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# textAngle{#textangle}

文本渲染方向。 指定用textPs=指定的文本排版并呈现到文本框中的角度（用size=或textFlowPath=定义）。

` textAngle= *`角度`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>方向角度（度）。 </p> </td> 
 </tr> 
</table>

正值将文本顺时针旋转；`textAngle=90`从上到下绘制文本。

## 属性 {#section-6d586a632daa4261a8ce62db56140b36}

图层属性。 如果`layer=comp`，则适用于`layer=0`。 如果未为此层指定`textPs=`或指定`textPath=`，则忽略。

## 默认 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` 不轮换。

## 另请参阅 {#section-dccc29ff33704061b2519b56b7be45fd}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [文本定](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)位 [，文](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)本Ps= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)textFlowPath= [,  Path=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
