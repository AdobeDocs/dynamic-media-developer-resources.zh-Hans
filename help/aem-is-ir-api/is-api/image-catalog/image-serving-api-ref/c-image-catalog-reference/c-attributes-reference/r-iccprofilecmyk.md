---
description: CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC颜色用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。
seo-description: CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC颜色用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于CMYK响应图像的ICC颜色用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。

## 属性 {#section-d8b6102cc1c744d482f99808ccfcaa24}

文本字符串。 如果指定，则必须是此图像目 `icc::Name` 录或默认目录的ICC用户档案映射中的有效值，或相对于的文件路径 `attribute::RootPath`。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-62442df09a724950bfbdd0640b3e6678}

如果未定义 `default::IccProfileCmyk` 或为空，则从中继承。

## 另请参阅 {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属性：:IccProfileSrcCmyk [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
