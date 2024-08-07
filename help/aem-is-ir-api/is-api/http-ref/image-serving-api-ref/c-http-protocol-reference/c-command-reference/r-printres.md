---
title: printRes
description: 打印分辨率。 覆盖响应图像中嵌入的打印分辨率值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# printRes{#printres}

打印分辨率。 覆盖响应图像中嵌入的打印分辨率值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>打印分辨率(dpi)。 </p></td> 
 </tr> 
</table>

如果打印分辨率是目录条目，则它通常由`catalog::PrintResolution`定义，否则由源图像中嵌入的打印分辨率值定义。 如果存在模板或分层复合图像，则响应文件中嵌入的默认打印分辨率是图层编号最低的图层图像的打印分辨率。

设置打印分辨率不会更改回复图像的像素大小。

## 属性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

请求属性。 无论当前图层设置如何，它都适用。

## 默认 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
或嵌入源图像中的打印分辨率。

## 另请参阅 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog：：PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
