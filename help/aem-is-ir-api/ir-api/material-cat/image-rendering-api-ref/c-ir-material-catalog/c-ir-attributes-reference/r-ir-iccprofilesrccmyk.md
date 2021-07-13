---
description: CMYK默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的CMYK材料图像的ICC颜色配置文件的名称。
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的CMYK材料图像的ICC颜色配置文件的名称。

## 属性 {#section-0cee77438d914c319ec876edb3490821}

文本字符串。 如果已指定，则必须是此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是CMYK配置文件。

## 默认 {#section-11f6239e0dd14827abf4a95c1b30161c}

从`default::IccProfileSrcCmyk`继承（如果未定义或为空）。 如果`attribute::IccProfileSrcCmyk`未解析为有效的配置文件，则将改用`attribute::IccProfileCmyk`。

## 另请参阅 {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [属性：:IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
