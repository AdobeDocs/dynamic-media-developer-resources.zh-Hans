---
description: RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的特定RGB颜色值。
seo-description: RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的特定RGB颜色值。
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的特定RGB颜色值。

## 属性 {#section-3cd753196959462e9e674dab0b033d08}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或者是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是RGB用户档案。

## 默认 {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

如果未定义或为空，则从`default::IccProfileSrcRgb`继承。 如果`attribute::IccProfileSrcRgb`未解析为有效用户档案，则使用`attribute::IccProfileRgb`。

## 另请参阅 {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
