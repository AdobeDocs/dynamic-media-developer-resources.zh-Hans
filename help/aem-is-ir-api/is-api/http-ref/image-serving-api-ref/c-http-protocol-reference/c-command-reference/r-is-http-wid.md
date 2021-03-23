---
description: 视图宽度。 指定在请求中fit=不存在时响应图像(视图图像)的宽度。
seo-description: 视图宽度。 指定在请求中fit=不存在时响应图像(视图图像)的宽度。
seo-title: wid
solution: Experience Manager
title: wid
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 3%

---


# wid{#wid}

视图宽度。 指定在请求中fit=不存在时响应图像(视图图像)的宽度。

` wid= *`瓦尔`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 瓦尔  </span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位，整数大于0）。 </p> </td> 
 </tr> 
</table>

如果同时指定了`hei=`和`scl=`，则可以根据`align=`属性裁剪复合图像。 当存在`fit=`时，`wid=`会指定精确、最小或最大响应图像宽度；有关详细信息，请参阅`fit=`的说明。

如果未指定`scl=`，则会缩放复合图像以适合。 如果同时指定了`wid=`和`hei=`，并且未指定`scl=`，则缩放图像以完全适合wid/hei矩形，使尽可能少的背景区域暴露。 在这种情况下，图像会根据`align=`属性放在视图矩形内。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 默认 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果未指定`wid=`、`hei=`和`scl=`，则回复图像将具有复合图像的大小或`attribute::DefaultPix`（以较小者为准）。

## 属性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

视图属性。 无论当前图层设置如何，均适用。

## 示例 {#section-82bc98b7c15a451bbe9b915d414c0470}

请求一幅图像以适合200x200矩形；如果图像不是正方形，则右上对齐图像。 任何背景区域都填有`attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同一图像，以200像素的固定宽度传送，但具有可变高度以保持图像的宽高比。 在这种情况下，返回的图像从没有任何背景填充区域。 请注意，在这种情况下，align=将不起作用。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另请参阅 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , fit= [, scl](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)=align= [,属](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)::DefaultPix  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) [,属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
