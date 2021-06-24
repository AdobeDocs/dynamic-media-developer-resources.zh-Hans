---
description: RGB默认输出颜色配置文件。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC颜色配置文件的名称，以及使用各种“图像提供”命令（如color=）指定的某些RGB颜色值的名称。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色配置文件。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC颜色配置文件的名称，以及使用各种“图像提供”命令（如color=）指定的某些RGB颜色值的名称。

## 属性 {#section-3dd55c954d4d4ad4bb715ed7cee31025}

文本字符串。 如果已指定，则必须是此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-dfe08dd7b851453ca816623a4179955b}

从`default::IccProfileRgb`继承（如果未定义或为空）。

## 另请参阅 {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [属性：:IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
