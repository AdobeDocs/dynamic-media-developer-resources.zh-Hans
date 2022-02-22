---
title: resMode
description: 重新取样模式。 选择重新取样和/或插值算法，以将渲染的图像缩放到使用wid=、hei=或scl=指定的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# resMode{#resmode}

重新取样模式。 选择重新取样和/或插值算法，以用于将渲染的图像缩放到指定的大小 `wid=`, `hei=`或 `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 比林 </span> </p> </td> 
   <td colname="col2"> <p>选择标准双线性插值。 最快的重新取样方法；某些锯齿伪影会相当明显。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>选择双立方插值。 与双线性插值相比，CPU密集度更高，但会生成较锐利的图像，出现的锯齿伪像较少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>选择修改的Lanczos窗口函数作为插值算法。 在CPU成本较高的情况下，可能会产生比双立方算法更锐利的结果。 </p> <p> <span class="codeph"> 锐 </span> 已被 <span class="codeph"> sharp2 </span>，导致出现锯齿伪像的可能性较小，也称为Moiré。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 比沙尔 </span> </p> </td> 
   <td colname="col2"> <p>选择 <span class="keyword"> Adobe Photoshop </span> 用于减小图像大小的默认重采样器(在 <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能发生在请求中的任何位置。 如果未应用最终图像缩放，则忽略。

## 默认 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另请参阅 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[属性：:ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
