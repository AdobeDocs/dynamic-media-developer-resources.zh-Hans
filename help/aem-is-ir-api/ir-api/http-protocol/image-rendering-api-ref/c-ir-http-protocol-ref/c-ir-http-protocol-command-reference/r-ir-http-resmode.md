---
title: 解析模式
description: 重新取样模式。 选择重新取样和/或插值算法，用于将渲染的图像缩放到以wid=、hei=或scl=指定的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# 解析模式{#resmode}

重新取样模式。 选择重新取样和/或插值算法，以将渲染的图像缩放到通过`wid=`、`hei=`或`scl=`指定的大小。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>选择标准的双线性插值。 最快的重新取样方法；某些锯齿伪影会相当明显。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>选择双三次插值。 比双线性插值占用更多的CPU资源，但生成更锐利的图像，出现的锯齿伪像较少。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph">锐化2 </span> </p> </td> 
   <td colname="col2"> <p>选择修改的Lanczos窗口函数作为插值算法。 可能会产生比双三次方更锐利的结果，但CPU成本会更高。 </p> <p> <span class="codeph"> sharp </span>已由<span class="codeph"> sharp2 </span>替换，该替换导致锯齿伪像（也称为Moiré）的可能性较小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">两次锐化</span> </p> </td> 
   <td colname="col2"> <p>选择<span class="keyword">Adobe Photoshop </span>用于减小图像大小的默认重新取样器，在<span class="keyword"> Adobe Photoshop </span>中称为“双立方更锐化”。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能出现在请求中的任何位置。 如果未应用最终图像缩放，则忽略。

## 默认 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另请参阅 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute：：ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ， [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
