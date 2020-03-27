---
description: 缩放视图。 按invFactor的反比缩放复合图像。
seo-description: 缩放视图。 按invFactor的反比缩放复合图像。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

No scaling is applied when `scl=1`. *`invFactor`* 大于1.0的缩小和小于1.0的缩小放大了复合图像。

如果 `scl=` 已指定，且 `wid=` 和／或 `hei=` 也存在，则图像会被裁剪到缩放 `wid=` 和/ `hei=` 或缩放后。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于，则返回错误 `attribute::MaxPix`。

## 属性 {#section-60af012719db477db4a4703e9a6da5f5}

视图属性。 无论当前图层设置如何，均可应用。

## 默认 {#section-32502fa218a24e1f9c65f41c0260b56a}

如果既 `wid=`未指 `hei=`定，也未指 `scl=` 定，则返回图像将具有复合图像的大小，或者以较小 `attribute::DefaultPix`的大小为准。

## 示例 {#section-a33f6239476a4b438d939656ad99aa76}

请参阅 [rotate=中的示例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ，了解的常见应用程序 `scl=`。

## 另请参阅 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)，属 [性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
