---
title: wid
description: 视图宽度。 指定请求中不存在fit=时响应图像（查看图像）的宽度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# wid{#wid}

视图宽度。 指定请求中不存在fit=时响应图像（查看图像）的宽度。

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>图像宽度，以像素为单位（int大于0）。 </p> </td> 
 </tr> 
</table>

如果同时指定了`hei=`和`scl=`，则可以根据`align=`属性裁剪复合图像。 当`fit=`存在时，`wid=`指定精确、最小或最大响应图像宽度；有关详细信息，请参阅`fit=`的说明。

如果未指定`scl=`，则将缩放复合图像以适合该图像。 如果同时指定了`wid=`和`hei=`，但未指定`scl=`，则图像将缩放以完全适合wid/hei矩形，从而保留尽可能少的背景区域。 在这种情况下，根据`align=`属性将图像放置在视图矩形内。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 默认 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果既未指定`wid=`、`hei=`也未指定`scl=`，则回复图像的大小为复合图像的大小或`attribute::DefaultPix`（取较小者）。

## 属性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

查看属性。 无论当前图层设置如何，它都适用。

## 示例 {#section-82bc98b7c15a451bbe9b915d414c0470}

请求图像以使其可放入200x200矩形中；如果图像非正方形，则右上角对齐图像。 任何背景区域都以`attribute::BkgColor`填充。

` http:// *`服务器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

相同的图像，以200像素的固定宽度投放，但具有可变高度以保持图像的宽高比。 在这种情况下，返回的图像从不包含任何背景填充区域。 在这种情况下，`align=`将没有任何效果。

` http:// *`服务器`*/myRootId/myImageId?wid=200`

## 另请参阅 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ，[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)，[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)，[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)，[attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)，[attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
