---
title: hei
description: 视图高度。 指定请求中不存在匹配时响应图像（查看图像）的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---

# hei{#hei}

视图高度。 指定请求中不存在匹配时响应图像（查看图像）的高度。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">变量</span> </span> </p> </td> 
  <td class="stentry"> <p>图像高度，以像素为单位（int大于0）。 </p> </td> 
 </tr> 
</table>

如果同时指定了`wid=`和`scl=`，则可以根据`align=`属性裁剪复合图像。 当`fit=`存在时，`hei=`指定确切的响应图像高度、最小响应图像高度或最大响应图像高度；有关详细信息，请参阅[fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md)的说明。

如果未指定`scl=`，则将缩放复合图像以适合该图像。 如果同时指定了`wid=`和`hei=`，但未指定`scl=`，则图像将缩放以完全适合wid/hei矩形，从而保留尽可能少的背景区域。 在这种情况下，根据`align=`属性将图像放置在视图矩形内。 背景区域已填满`bgc=`，如果未使用`attribute::BkgColor`指定，则填满。

>[!NOTE]
>
>如果计算的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-534923644a1e464496eeba83dedcbd3c}

查看属性。 无论当前图层设置如何，它都适用。

## 默认 {#section-76544d34806d4124a8b173e229cba71f}

如果既未指定`wid=`、`hei=`也未指定`scl=`，则回复图像的大小为复合图像的大小或`attribute::DefaultPix`（取较小者）。

## 示例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

请求图像以使其可放入200x200矩形中；如果图像非正方形，则左上角对齐图像。 任何背景区域都以`attribute::BkgColor`填充。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

相同的图像，以200像素的固定高度交付，但具有匹配图像宽高比的可变宽度。 在这种情况下，返回的图像从不包含任何背景填充区域。 在这种情况下，`align=`将没有任何效果。

`http://server/myRootId/myImageId?hei=200`

## 另请参阅 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ，[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)，[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)，[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)，[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)，[rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)，[attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)，[attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
