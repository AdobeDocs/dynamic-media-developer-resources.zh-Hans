---
description: CMYK默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的CMYK源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。
seo-description: CMYK默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的CMYK源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的CMYK源图像的ICC颜色用户档案的名称，以及用于使用各种图像服务命令（如color=）指定的某些CMYK颜色值的名称。

## 属性 {#section-fc2ad12a3c6e4c7cab495f1878638e66}

文本字符串。 如果指定，则必须是此图像目 `icc::Name` 录或默认目录的ICC用户档案映射中的有效值，或相对于的文件路径 `attribute::RootPath`。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

如果未定义 `default::IccProfileSrcCmyk` 或为空，则从中继承。 如 `attribute::IccProfileSrcCmyk` 果未解析为有效用户档案，则 `attribute::IccProfileCmyk` 使用它。

## 另请参阅 {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属性：:IccProfileCmyk [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
