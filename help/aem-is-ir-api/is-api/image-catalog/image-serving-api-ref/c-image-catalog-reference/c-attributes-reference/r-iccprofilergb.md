---
description: RGB默认输出颜色配置文件。 指定在通过icc=未指定输出色彩空间时用于RGB响应图像的ICC色彩配置文件的名称，以及指定通过各种“图像提供”命令（如color=）指定的某些RGB色彩值的名称。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色配置文件。 指定在通过icc=未指定输出色彩空间时用于RGB响应图像的ICC色彩配置文件的名称，以及指定通过各种“图像提供”命令（如color=）指定的某些RGB色彩值的名称。

## 属性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文本字符串。 如果指定，则必须为此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或者相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-dfe08dd7b851453ca816623a4179955b}

如果未定义或为空，则从`default::IccProfileRgb`继承。

## 另请参阅 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)，[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
