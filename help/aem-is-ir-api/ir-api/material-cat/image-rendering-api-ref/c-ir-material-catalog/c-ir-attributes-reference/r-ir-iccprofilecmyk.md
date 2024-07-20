---
title: IccProfileCmyk
description: CMYK默认颜色空间。 指定当没有使用icc=指定输出色彩空间时，用于灰度响应图像的ICC色彩配置文件的名称。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

CMYK默认颜色空间。 指定当没有使用`icc=`指定输出色彩空间时用于灰度响应图像的ICC色彩配置文件的名称。

## 属性 {#section-849678b272954bdcb236f49aa54f1609}

文本字符串。 如果指定，则必须为此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或者相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是CMYK配置文件。

## 默认 {#section-55026b7454af4d868bcb47f7743c9c5b}

如果未定义或为空，则从`default::IccProfileCmyk`继承。

## 另请参阅 {#section-89feb193693b43dc99a2107658d57154}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，[attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[attribute：：IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
