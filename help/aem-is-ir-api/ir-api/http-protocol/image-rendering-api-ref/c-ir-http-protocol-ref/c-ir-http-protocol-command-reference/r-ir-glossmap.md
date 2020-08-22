---
description: 光泽地图图像。 提供对可重复纹理、墙纸／边框或阴影光泽度的逐像素控制。
seo-description: 光泽地图图像。 提供对可重复纹理、墙纸／边框或阴影光泽度的逐像素控制。
seo-title: 舌面图
solution: Experience Manager
title: 舌面图
topic: Scene7 Image Serving - Image Rendering API
uuid: f137d362-74a1-45b3-9274-a3a2d6cf5db0
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# 舌面图{#glossmap}

光泽地图图像。 提供对可重复纹理、墙纸／边框或阴影光泽度的逐像素控制。

`glossmap={ *``*| *`GlossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrace;'is&amp;<span class="varname"> 'isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> forieReq</span>'&amp;rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>光泽图图像文件（灰度）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>请求到图像服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>请求到外部服务器。 </p></td> 
 </tr> 
</table>

适用于金属涂料效果、模切箔壁纸和边框、金属线织物等材料。

光泽映射图像必须为8位灰度，且大小与使用指定的主图像完全相同 `src=`。 有关其他信息，请参 [ 阅的 `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 说明。

## 属性 {#section-26375672d69849be9b026cc93c3bc558}

材料属性。 支持可重复的纹理、墙纸和边框以及装饰。 被纯色、机柜和窗口覆盖材料忽略。 请参 [ 阅以了 `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 解更多信息。

## 默认 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

无。

## 另请参阅 {#section-33953fc1be82452da37141f2e541e00c}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
