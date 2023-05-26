---
title: IccProfileSrcRgb
description: RGB默认输入颜色配置文件。 指定用于RGB材质图像和不嵌入颜色配置文件的晕影的ICC颜色配置文件的名称。 此外，还适用于通过各种“图像渲染”命令（例如bgc=和color=）指定的RGB颜色值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB默认输入颜色配置文件。 指定用于RGB材质图像和不嵌入颜色配置文件的晕影的ICC颜色配置文件的名称。 RGB对于通过各种“图像渲染”命令(例如 `bgc=` 和 `color=`.

## 属性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文本字符串。 如果指定，则必须为有效 `icc::Name` 值，该值来自此图像目录或默认目录的ICC配置文件映射，或相对于该图像目录的文件路径 `attribute::RootPath`. 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-0171cd6680284bfa9844b9cc3644ca61}

继承自 `default::IccProfileSrcRgb` 如果未定义或为空。 如果 `attribute::IccProfileSrcRgb` 无法解析为有效的配置文件， `attribute::IccProfileRgb` 而使用。

## 另请参阅 {#section-1ba91666830f4c209c39260ea29f938e}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [attribute：：IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
