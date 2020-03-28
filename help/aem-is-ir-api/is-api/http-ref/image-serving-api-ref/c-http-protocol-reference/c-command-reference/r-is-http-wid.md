---
description: 视图宽度。 当fit=在请求中不存在时，指定响应图像(视图图像)的宽度。
seo-description: 视图宽度。 当fit=在请求中不存在时，指定响应图像(视图图像)的宽度。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

视图宽度。 当fit=在请求中不存在时，指定响应图像(视图图像)的宽度。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位）（大于0的整数）。 </p> </td> 
 </tr> 
</table>

如果同时 `hei=` 指定 `scl=` 了和，则可以根据属性裁剪复合图 `align=` 像。 当存 `fit=` 在时，指 `wid=` 定精确、最小或最大响应图像宽度；有关详细信息，请参阅的 `fit=` 说明。

如果 `scl=` 未指定，则会缩放合成图像以适合。 如果同时 `wid=` 指定和 `hei=``scl=` 未指定，则缩放图像以完全适合宽／高矩形，使尽可能少的背景区域暴露出来。 在这种情况下，图像会根据属性放在视图矩形内 `align=` 。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于，则返回错误 `attribute::MaxPix`。

## 默认 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果既 `wid=`未指 `hei=`定，也未指 `scl=` 定，则返回图像将具有复合图像的大小，或者以较小 `attribute::DefaultPix`的大小为准。

## 属性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

视图属性。 无论当前图层设置如何，均可应用。

## 示例 {#section-82bc98b7c15a451bbe9b915d414c0470}

请求一幅图像以适合200x200的矩形；如果图像不是正方形，则右上对齐图像。 任何背景区域都会填充 `attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同一图像，以200像素的固定宽度传送，但具有可变高度以保持图像的宽高比。 在这种情况下，返回的图像从来没有任何背景填充区域。 请注意，在这种情况下，align=根本不起作用。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另请参阅 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , fit= [, scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), align= [，属性：](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[Pix:Default Pix, DefaultPix属性：:MaxMaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
