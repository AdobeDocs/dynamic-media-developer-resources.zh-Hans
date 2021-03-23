---
description: 视图高度. 指定在请求中不存在适合时响应图像(视图图像)的高度。
seo-description: 视图高度. 指定在请求中不存在适合时响应图像(视图图像)的高度。
seo-title: hei
solution: Experience Manager
title: 平
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 4%

---


# hei{#hei}

视图高度. 指定在请求中不存在适合时响应图像(视图图像)的高度。

` hei= *`瓦尔`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>图像高度（以像素为单位，整数大于0）。 </p> </td> 
 </tr> 
</table>

如果同时指定了`wid=`和`scl=`，则可以根据`align=`属性裁剪复合图像。 当存在`fit=`时，`hei=`指定精确、最小或最大响应图像高度；有关详细信息，请参阅` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`的说明。

如果未指定`scl=`，则会缩放复合图像以适合。 如果同时指定了`wid=`和`hei=`，并且未指定`scl=`，则缩放图像以完全适合宽/黑矩形，使尽可能少的背景区域暴露；在这种情况下，图像会根据`align=`属性放在视图矩形内。 背景区域填充有`bgc=`，如果未用`attribute::BkgColor`指定。

>[!NOTE]
>
>如果计算的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-534923644a1e464496eeba83dedcbd3c}

视图属性。 无论当前图层设置如何，均适用。

## 默认 {#section-76544d34806d4124a8b173e229cba71f}

如果既未指定`wid=`、`hei=`或`scl=`，则返回图像的大小为复合图像的大小或`attribute::DefaultPix`（以较小者为准）。

## 示例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

请求一幅图像以适合200x200矩形；如果图像不是正方形，则左上对齐图像。 任何背景区域都填有`attribute::BkgColor`。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同一图像，以200像素的固定高度传送，但宽度可变以匹配图像的宽高比。 在这种情况下，返回的图像从没有任何背景填充区域。 请注意，在这种情况下，`align=`根本不起作用。

`http://server/myRootId/myImageId?hei=200`

## 另请参阅 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , fit [=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), scl= [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) [ bgc=, , =,  Pix属性：:Default Pix Pix属性：:DefaultPix，属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
