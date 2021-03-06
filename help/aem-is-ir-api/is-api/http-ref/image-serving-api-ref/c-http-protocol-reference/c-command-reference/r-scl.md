---
description: 缩放视图。 按invFactor的反比缩放复合图像。
solution: Experience Manager
title: scl
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# scl{#scl}

缩放视图。 按invFactor的反比缩放复合图像。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>反比例因子（实数大于0.0）。 </p></td> 
 </tr> 
</table>

`scl=1`时不应用缩放。 *`invFactor`* 大于1.0的缩放和小于1.0会放大复合图像。

如果指定了`scl=`，并且还存在`wid=`和/或`hei=`，则缩放后会将图像裁剪到`wid=`和/或`hei=`。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-60af012719db477db4a4703e9a6da5f5}

查看属性。 无论当前的层设置如何，都适用。

## 默认 {#section-32502fa218a24e1f9c65f41c0260b56a}

如果未指定`wid=`、`hei=`和`scl=`，则返回图像的大小将为复合图像的大小或`attribute::DefaultPix`（以较小者为准）。

## 示例 {#section-a33f6239476a4b438d939656ad99aa76}

有关`scl=`的常见应用程序，请参阅[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)中的示例。

## 另请参阅 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)，属 [性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
