---
title: scl
description: 缩放视图。 按invFactor的逆比例缩放复合图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# scl{#scl}

缩放视图。 按invFactor的逆比例缩放复合图像。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>反比例因子（实数大于0.0）。 </p></td> 
 </tr> 
</table>

`scl=1`时未应用任何缩放。 大于1.0的&#x200B;*`invFactor`*&#x200B;值是缩小的值，小于1.0则会放大复合图像。

如果指定了`scl=`，并且也存在`wid=`和/或`hei=`，则在缩放后将图像裁剪为`wid=`和/或`hei=`。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-60af012719db477db4a4703e9a6da5f5}

查看属性。 无论当前图层设置如何，它都适用。

## 默认 {#section-32502fa218a24e1f9c65f41c0260b56a}

如果既未指定`wid=`、`hei=`也未指定`scl=`，则回复图像的大小为复合图像的大小或`attribute::DefaultPix`（取较小者）。

## 示例 {#section-a33f6239476a4b438d939656ad99aa76}

请参阅[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)中的示例，了解`scl=`的常用应用程序。

## 另请参阅 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ，[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)，[attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
