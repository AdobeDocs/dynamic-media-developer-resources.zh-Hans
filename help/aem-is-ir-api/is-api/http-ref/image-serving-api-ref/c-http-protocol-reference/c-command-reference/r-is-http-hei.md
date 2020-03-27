---
description: 视图高度. 指定当请求中不存在适合时响应图像(视图图像)的高度。
seo-description: 视图高度. 指定当请求中不存在适合时响应图像(视图图像)的高度。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

视图高度. 指定当请求中不存在适合时响应图像(视图图像)的高度。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>图像高度（以像素为单位）（大于0的整数）。 </p> </td> 
 </tr> 
</table>

如果同时 `wid=` 指定 `scl=` 了和，则可以根据属性裁剪复合 `align=`图像。 当存 `fit=` 在时，指定 `hei=` 精确、最小或最大响应图像高度；有关详细信息，请参阅的 ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` 说明。

如果 `scl=` 未指定，则会缩放合成图像以适合。 如果既 `wid=` 指定了 `hei=` ，又未指定， `scl=` 则对图像进行缩放以完全适合宽／高矩形，使背景区域尽可能小；在这种情况下，图像会根据属性放在视图矩形内 `align=` 。 背景区域将填充， `bgc=`或者，如果未指定 `attribute::BkgColor`。

>[!NOTE]
>
>如果计算的回复图像大小大于此值，则返回错误 `attribute::MaxPix`。

## 属性 {#section-534923644a1e464496eeba83dedcbd3c}

视图属性。 无论当前图层设置如何，均可应用。

## 默认 {#section-76544d34806d4124a8b173e229cba71f}

如果既 `wid=`未指 `hei=`定，也未指 `scl=` 定，则返回图像具有复合图像的大小，或者以较小 `attribute::DefaultPix`的大小为准。

## 示例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

请求一幅图像以适合200x200的矩形；如果图像不是正方形，则左上对齐图像。 任何背景区域都会填充 `attribute::BkgColor`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同一图像，以200像素的固定高度传送，但宽度可变以匹配图像的长宽比。 在这种情况下，返回的图像从来没有任何背景填充区域。 请注意，在这种情 `align=` 况下，根本不起作用。

`http://server/myRootId/myImageId?hei=200`

## 另请参阅 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) fit= [, scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [align=,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)balign=, [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[bgc=, rgn=Default Pix属性：:Adobe Pix属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
