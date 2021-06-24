---
description: CMYK默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的CMYK源图像的ICC颜色配置文件的名称，以及使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的CMYK源图像的ICC颜色配置文件的名称，以及使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。

## 属性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文本字符串。 如果已指定，则必须是此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是CMYK配置文件。

## 默认 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

从`default::IccProfileSrcCmyk`继承（如果未定义或为空）。 如果`attribute::IccProfileSrcCmyk`未解析为有效的配置文件，则使用`attribute::IccProfileCmyk`。

## 另请参阅 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [属性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
