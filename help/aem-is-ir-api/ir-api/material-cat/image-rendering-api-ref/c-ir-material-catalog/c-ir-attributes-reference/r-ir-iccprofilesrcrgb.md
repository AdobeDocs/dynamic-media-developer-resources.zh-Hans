---
description: RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB材料图像和晕影的ICC颜色用户档案的名称，以及用于使用各种图像渲染命令（如bgc=和color=）指定的RGB颜色值的名称。
seo-description: RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB材料图像和晕影的ICC颜色用户档案的名称，以及用于使用各种图像渲染命令（如bgc=和color=）指定的RGB颜色值的名称。
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB默认输入颜色用户档案。 指定用于不嵌入颜色用户档案的RGB材料图像和晕影的ICC颜色用户档案的名称，以及用于使用各种图像渲染命令（如bgc=和color=）指定的RGB颜色值的名称。

## 属性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文本字符串。 如果指定，则必须是此图像目 `icc::Name` 录或默认目录的ICC用户档案映射中的有效值，或相对于的文件路径 `attribute::RootPath`。 引用的ICC用户档案必须是RGB用户档案。

## 默认 {#section-0171cd6680284bfa9844b9cc3644ca61}

如果未定义 `default::IccProfileSrcRgb` 或为空，则从中继承。 如 `attribute::IccProfileSrcRgb` 果未解析为有效用户档案，则 `attribute::IccProfileRgb` 使用它。

## 另请参阅 {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属性：:IccProfileRgb [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
