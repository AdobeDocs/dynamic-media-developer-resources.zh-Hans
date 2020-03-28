---
description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种图像服务命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。
seo-description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种图像服务命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种图像服务命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。

## 属性 {#section-8cbb316df6eb463aaca7b308d3568086}

文本字符串。 如果指定，则必须是此图像目 `icc::Name` 录或默认目录的ICC用户档案映射中的有效值，或相对于的文件路径 `attribute::RootPath`。 引用的ICC用户档案必须是灰度用户档案。

## 默认 {#section-bcc7250715884412bd0780f60d1cce7b}

如果未定义 `default::IccProfileSrcGray` 或为空，则从中继承。 如 `attribute::IccProfileSrcGray` 果未解析为有效用户档案，则 `attribute::IccProfileGray` 使用它。

## 另请参阅 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属性：:IccProfileGray [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
