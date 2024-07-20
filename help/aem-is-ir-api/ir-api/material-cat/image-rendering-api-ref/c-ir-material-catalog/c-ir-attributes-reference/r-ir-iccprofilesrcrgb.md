---
title: IccProfileSrcRgb
description: 默认输入RGB配置文件。 指定用于RGB材质图像和不嵌入颜色配置文件的晕影的ICC颜色配置文件的名称。 对于通过各种“图像渲染”命令（例如bgc=和color=）指定的RGB颜色值，也是如此。
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

默认输入RGB配置文件。 指定用于RGB材质图像和不嵌入颜色配置文件的晕影的ICC颜色配置文件的名称。 此外，对于通过各种图像渲染命令（如`bgc=`和`color=`）指定的RGB颜色值。

## 属性 {#section-c22966bba03e43c08e9d3fb91bfdd465}

文本字符串。 如果指定，则必须为此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或者相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-0171cd6680284bfa9844b9cc3644ca61}

如果未定义或为空，则从`default::IccProfileSrcRgb`继承。 如果`attribute::IccProfileSrcRgb`未解析为有效的配置文件，则改用`attribute::IccProfileRgb`。

## 另请参阅 {#section-1ba91666830f4c209c39260ea29f938e}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，[attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[attribute：：IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
