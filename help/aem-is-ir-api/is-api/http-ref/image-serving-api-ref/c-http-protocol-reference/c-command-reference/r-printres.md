---
description: 打印分辨率。 覆盖嵌入在响应图像中的打印分辨率值。
seo-description: 打印分辨率。 覆盖嵌入在响应图像中的打印分辨率值。
seo-title: printRes
solution: Experience Manager
title: printRes
uuid: 1a62611a-b3b9-4f20-834f-e34e75d33ddd
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# printRes{#printres}

打印分辨率。 覆盖嵌入在响应图像中的打印分辨率值。

`printRes= *`瓦尔`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 瓦尔</span> </p> </td> 
  <td class="stentry"> <p>打印分辨率(dpi)。 </p></td> 
 </tr> 
</table>

打印分辨率通常由`catalog::PrintResolution`定义（如果是目录条目），否则由嵌入在源图像中的打印分辨率值定义。 如果是模板或分层复合图像，则嵌入响应文件中的默认打印分辨率是具有最低图层编号的图层图像的打印分辨率。

设置打印分辨率不会更改回复图像的像素大小。

## 属性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

请求属性。 无论当前图层设置如何，均适用。

## 默认 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或嵌入源图像中的打印分辨率。

## 另请参阅 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
