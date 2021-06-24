---
description: 光泽地图图像。 对可重复纹理、墙纸/边框或贴图的光泽度进行逐像素控制。
solution: Experience Manager
title: 词汇表
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---

# 词汇表{#glossmap}

光泽地图图像。 对可重复纹理、墙纸/边框或贴图的光泽度进行逐像素控制。

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;lbrase;'is&amp;lbrase;'<span class="varname"> isReq</span>'&amp;rbrase;'&amp;rbrase;|&amp;lbrase;'&amp;lbrase;'<span class="varname"> foreignReq</span>'&amp;rbrase;'  </span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>请求到外部服务器。 </p></td> 
 </tr> 
</table>

适用于金属漆效果、模切箔壁纸、边框、金属丝织物等材料。

光泽图图像必须为8位灰度，并且与使用`src=`指定的主图像大小完全相同。 有关其他信息，请参阅[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)的说明。

## 属性 {#section-26375672d69849be9b026cc93c3bc558}

材料属性。 由可重复的纹理、壁纸和边框以及贴图提供支持。 被实色、机柜和窗口覆盖材料忽略。 有关其他信息，请参阅[ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) 。

## 默认 {#section-d9ac031fb2f94482ac3fe2283d7cb168}

无。

## 另请参阅 {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
