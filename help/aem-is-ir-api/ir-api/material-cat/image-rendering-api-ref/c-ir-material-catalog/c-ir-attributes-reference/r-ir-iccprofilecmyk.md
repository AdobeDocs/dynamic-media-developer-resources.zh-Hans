---
description: CMYK默认色彩空间。 指定在未使用icc=指定输出色彩空间时用于灰度级响应图像的ICC颜色配置文件的名称。
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK默认色彩空间。 指定在未使用icc=指定输出色彩空间时用于灰度级响应图像的ICC颜色配置文件的名称。

## 属性 {#section-849678b272954bdcb236f49aa54f1609}

文本字符串。 如果已指定，则必须是此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是CMYK配置文件。

## 默认 {#section-55026b7454af4d868bcb47f7743c9c5b}

从`default::IccProfileCmyk`继承（如果未定义或为空）。

## 另请参阅 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [属性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2),  [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
