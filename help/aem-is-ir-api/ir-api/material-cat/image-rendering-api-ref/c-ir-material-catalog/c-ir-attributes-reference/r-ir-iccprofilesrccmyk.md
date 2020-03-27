---
description: CMYK默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的CMYK材料图像的ICC颜色用户档案的名称。
seo-description: CMYK默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的CMYK材料图像的ICC颜色用户档案的名称。
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的CMYK材料图像的ICC颜色用户档案的名称。

## 属性 {#section-0cee77438d914c319ec876edb3490821}

文本字符串。 如果指定，则必须是此图像目 `icc::Name` 录或默认目录的ICC用户档案映射中的有效值，或相对于的文件路径 `attribute::RootPath`。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-11f6239e0dd14827abf4a95c1b30161c}

如果未定义 `default::IccProfileSrcCmyk` 或为空，则从中继承。 如 `attribute::IccProfileSrcCmyk` 果未解析为有效用户档案，则 `attribute::IccProfileCmyk` 将使用它。

## 另请参阅 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属性：:IccProfileCmyk [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
