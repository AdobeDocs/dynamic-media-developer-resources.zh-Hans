---
description: CMYK默认输出颜色配置文件。 指定当没有使用icc=指定输出色彩空间时，用于CMYK响应图像的ICC色彩配置文件的名称，以及指定各种图像服务命令（例如color=）所指定的某些CMYK色彩值的名称。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK默认输出颜色配置文件。 指定当没有使用icc=指定输出色彩空间时，用于CMYK响应图像的ICC色彩配置文件的名称，以及指定各种图像服务命令（例如color=）所指定的某些CMYK色彩值的名称。

## 属性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文本字符串。 如果指定，则必须为有效 `icc::Name` 值，该值来自此图像目录或默认目录的ICC配置文件映射，或相对于该图像目录的文件路径 `attribute::RootPath`. 引用的ICC配置文件必须是CMYK配置文件。

## 默认 {#section-62442df09a724950bfbdd0640b3e6678}

继承自 `default::IccProfileCmyk` 如果未定义或为空。

## 另请参阅 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [属性：：IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
