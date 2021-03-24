---
description: CMYK默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的CMYK源图像的ICC颜色用户档案的名称，以及用各种"图像服务"命令（如color=）指定的某些CMYK颜色值的名称。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的CMYK源图像的ICC颜色用户档案的名称，以及用各种&quot;图像服务&quot;命令（如color=）指定的某些CMYK颜色值的名称。

## 属性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

如果未定义或为空，则从`default::IccProfileSrcCmyk`继承。 如果`attribute::IccProfileSrcCmyk`未解析为有效用户档案，则使用`attribute::IccProfileCmyk`。

## 另请参阅 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
