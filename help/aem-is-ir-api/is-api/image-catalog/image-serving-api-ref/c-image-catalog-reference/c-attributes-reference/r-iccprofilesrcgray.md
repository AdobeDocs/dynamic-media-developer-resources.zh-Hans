---
description: 灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度源图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的名称。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度源图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的名称。

## 属性 {#section-8cbb316df6eb463aaca7b308d3568086}

文本字符串。 如果指定，则必须为有效 `icc::Name` 值，该值来自此图像目录或默认目录的ICC配置文件映射，或相对于该图像目录的文件路径 `attribute::RootPath`. 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-bcc7250715884412bd0780f60d1cce7b}

继承自 `default::IccProfileSrcGray` 如果未定义或为空。 如果 `attribute::IccProfileSrcGray` 无法解析为有效的配置文件， `attribute::IccProfileGray` 而使用。

## 另请参阅 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [attribute：：IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
