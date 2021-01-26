---
description: 重新取样模式。 选择重新取样和／或插值算法以将渲染的图像缩放到用wid=、hei=或scl=指定的大小。
seo-description: 重新取样模式。 选择重新取样和／或插值算法以将渲染的图像缩放到用wid=、hei=或scl=指定的大小。
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# resMode{#resmode}

重新取样模式。 选择重新取样和／或插值算法以将渲染的图像缩放到用wid=、hei=或scl=指定的大小。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比林  </span> </p> </td> 
   <td colname="col2"> <p>选择标准双线性插值。 最快的重新取样方法；某些锯齿伪影会相当明显。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比克布  </span> </p> </td> 
   <td colname="col2"> <p>选择双立方插值。 与双线性插值相比，CPU占用更多，但会生成更锐利的图像，并且出现的锯齿伪像较少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>选择修改的Lanczos窗函数作为插值算法。 在CPU成本较高的情况下，可能产生比双立方图像更锐利的结果。 </p> <p> <span class="codeph"> sharp </span> 已被sharp2 <span class="codeph"> 所取代， </span>它产生锯齿伪像的可能性较小，也称为Moiré。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙尔  </span> </p> </td> 
   <td colname="col2"> <p>选择<span class="keyword">Adobe Photoshop</span>默认重新取样器以减小图像大小，在<span class="keyword">Adobe Photoshop</span>中，该取样器称为“双立方锐化”。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能在请求中的任何位置发生。 如果未应用最终图像缩放，则忽略此项。

## 默认 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另请参阅 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[属性：:ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)=,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
