---
description: CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC色彩用户档案的名称，以及使用各种“图像服务”命令（如color=）指定的某些CMYK颜色值。
seo-description: CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC色彩用户档案的名称，以及使用各种“图像服务”命令（如color=）指定的某些CMYK颜色值。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC色彩用户档案的名称，以及使用各种“图像服务”命令（如color=）指定的某些CMYK颜色值。

## 属性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或者是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-62442df09a724950bfbdd0640b3e6678}

如果未定义或为空，则从`default::IccProfileCmyk`继承。

## 另请参阅 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
