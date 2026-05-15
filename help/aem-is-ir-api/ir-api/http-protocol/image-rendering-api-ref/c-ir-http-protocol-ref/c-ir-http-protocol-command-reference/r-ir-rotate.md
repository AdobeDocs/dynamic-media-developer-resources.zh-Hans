---
title: 旋轉
description: 材料旋转角度。 定义材料的旋转角度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

---

# 旋轉{#rotate}

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

材质属性。 已被纯色、墙纸、机柜和窗口处理材料忽略。*`angle`* 对于可重复纹理，必须是45的倍数，除非应用于Flowline或Sketch对象。

## 默认 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`，表示无轮换。

## 另请参阅 {#section-f73c00e9368b478dac1fd15bb4367a12}

[锚点=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
