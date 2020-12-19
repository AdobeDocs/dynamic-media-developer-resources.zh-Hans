---
description: RGB默认输出颜色用户档案。 指定在未用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些RGB色彩值。
seo-description: RGB默认输出颜色用户档案。 指定在未用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些RGB色彩值。
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色用户档案。 指定在未用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种图像服务命令（如color=）指定的某些RGB色彩值。

## 属性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或者是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是RGB用户档案。

## 默认 {#section-dfe08dd7b851453ca816623a4179955b}

如果未定义或为空，则从`default::IccProfileRgb`继承。

## 另请参阅 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
