---
description: 材料旋转角度。 定义材料的旋转角度。
seo-description: 材料旋转角度。 定义材料的旋转角度。
seo-title: 旋转
solution: Experience Manager
title: 旋转
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rotate{#rotate}

材料旋转角度。 定义材料的旋转角度。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>旋转角度（以度为单位）。 </p> </td> 
 </tr> 
</table>

当应用于平面对象或平面对象时，可重复的纹理材料（不包括壁纸）旋转45度的倍数。

在应用于流线和草图对象时，将可重复的纹理材料旋转任意角度。

按任意角度旋转倾斜的材料。

正角度顺时针旋转。 纹理或倾斜体绕锚点旋转( `anchor=`);锚点与目标对象的来源保持一致。

## 属性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材料属性。 被纯色、墙纸、橱柜和窗处理材料忽略。 *`angle`* 对于可重复的纹理，必须是45的倍数，除非应用于流线或草图对象。

## 默认 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，不旋转。

## 另请参阅 {#section-f73c00e9368b478dac1fd15bb4367a12}

[锚记=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
