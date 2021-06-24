---
description: RGB默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的RGB源图像的ICC颜色配置文件的名称，以及使用各种“图像提供”命令（如color=）指定的某些RGB颜色值的名称。
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的RGB源图像的ICC颜色配置文件的名称，以及使用各种“图像提供”命令（如color=）指定的某些RGB颜色值的名称。

## 属性 {#section-3cd753196959462e9e674dab0b033d08}

文本字符串。 如果已指定，则必须是此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

从`default::IccProfileSrcRgb`继承（如果未定义或为空）。 如果`attribute::IccProfileSrcRgb`未解析为有效的配置文件，则使用`attribute::IccProfileRgb`。

## 另请参阅 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [属性：:IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
