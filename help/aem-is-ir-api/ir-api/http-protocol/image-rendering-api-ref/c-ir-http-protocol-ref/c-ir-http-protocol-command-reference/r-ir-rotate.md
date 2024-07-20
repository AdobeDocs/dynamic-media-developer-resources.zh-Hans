---
title: 旋转
description: 材料旋转角度。 定义材料的旋转角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# 旋转{#rotate}

材料旋转角度。 定义材料的旋转角度。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>旋转角度，以度为单位（实数）。 </p> </td> 
 </tr> 
</table>

应用于平面对象或平面对象时，将可重复的纹理材料（不包括墙纸）旋转45°的倍数。

将可重复的纹理材料旋转任意角度（当应用于“流线”和“草绘对象”时）。

按任意角度旋转贴花材料。

正角度顺时针旋转。 纹理或贴花围绕锚点(`anchor=`)旋转；锚点保持与目标对象的原点对齐。

## 属性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材质属性。 已被纯色、墙纸、机柜和窗口处理材料忽略。 对于可重复纹理，*`angle`*&#x200B;必须是45的倍数，除非应用于Flowline或Sketch对象。

## 默认 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，表示无轮换。

## 另请参阅 {#section-f73c00e9368b478dac1fd15bb4367a12}

[锚点=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
