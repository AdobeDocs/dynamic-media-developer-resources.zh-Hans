---
title: 文本角度
description: 文本渲染方向。 指定使用textPs=指定的文本布局并渲染到文本框中的角度（使用size=或textFlowPath=定义）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# 文本角度{#textangle}

文本渲染方向。 指定使用textPs=指定的文本布局并渲染到文本框中的角度（使用size=或textFlowPath=定义）。

` textAngle= *`角度`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>方向角（度）。 </p> </td> 
 </tr> 
</table>

正值将文本顺时针旋转；`textAngle=90`从上到下绘制文本。

## 属性 {#section-6d586a632daa4261a8ce62db56140b36}

层属性。 应用于`layer=0`（如果`layer=comp`）。 如果未为此层指定`textPs=`或指定了`textPath=`，则忽略。

## 默认 {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0`表示无轮换。

## 另请参阅 {#section-dccc29ff33704061b2519b56b7be45fd}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)，[文本位置](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)，[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)，[textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)，[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
