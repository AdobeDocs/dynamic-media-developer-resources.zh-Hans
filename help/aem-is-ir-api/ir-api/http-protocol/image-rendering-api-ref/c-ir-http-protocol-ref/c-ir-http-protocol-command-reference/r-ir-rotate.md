---
description: 材料旋转角度。 定义材料的旋转角度。
solution: Experience Manager
title: 旋转
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# 旋转{#rotate}

材料旋转角度。 定义材料的旋转角度。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>旋转角度（以度为单位）。 </p> </td> 
 </tr> 
</table>

当应用于“平面对象”或“平面对象”时，可重复的纹理材料（不包括壁纸）旋转45度的倍数。

在应用于流线和草图对象时，按任意角度旋转可重复纹理材料。

按任意角度旋转倾斜材料。

正角度顺时针旋转。 纹理或倾斜体绕锚点旋转(`anchor=`);锚点与目标对象的源保持一致。

## 属性 {#section-ad4d07897ca24f63af1a4062f8618e36}

材料属性。 被纯色、墙纸、机柜和窗口处理材料忽略。 *`angle`* 对于可重复的纹理，必须是45的倍数，除非应用于流线或草图对象。

## 默认 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，不旋转。

## 另请参阅 {#section-f73c00e9368b478dac1fd15bb4367a12}

[锚记=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
