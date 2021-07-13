---
description: 打印分辨率。 覆盖响应图像中嵌入的打印分辨率值。
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

打印分辨率。 覆盖响应图像中嵌入的打印分辨率值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>打印分辨率(dpi)。 </p></td> 
 </tr> 
</table>

对于目录条目，打印分辨率通常由`catalog::PrintResolution`定义，否则由嵌入在源图像中的打印分辨率值定义。 对于模板或分层复合图像，在响应文件中嵌入的默认打印分辨率是具有最低图层编号的图层图像的打印分辨率。

设置打印分辨率不会更改回复图像的像素大小。

## 属性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

请求属性。 无论当前的层设置如何，都适用。

## 默认 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或嵌入源图像中的打印分辨率。

## 另请参阅 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
