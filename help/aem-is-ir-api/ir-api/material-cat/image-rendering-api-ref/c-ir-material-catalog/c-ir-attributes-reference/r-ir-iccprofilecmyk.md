---
description: CMYK默认色彩空间。 指定在未用icc=指定输出色彩空间时用于灰度响应图像的ICC颜色用户档案的名称。
seo-description: CMYK默认色彩空间。 指定在未用icc=指定输出色彩空间时用于灰度响应图像的ICC颜色用户档案的名称。
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

CMYK默认色彩空间。 指定在未用icc=指定输出色彩空间时用于灰度响应图像的ICC颜色用户档案的名称。

## 属性 {#section-849678b272954bdcb236f49aa54f1609}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或者是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是CMYK用户档案。

## 默认 {#section-55026b7454af4d868bcb47f7743c9c5b}

如果未定义或为空，则从`default::IccProfileCmyk`继承。

## 另请参阅 {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属 [性：:IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
