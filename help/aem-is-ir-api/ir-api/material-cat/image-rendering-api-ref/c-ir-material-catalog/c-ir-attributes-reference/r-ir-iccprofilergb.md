---
title: IccProfileRgb
description: RGB默认输出颜色配置文件。 指定当没有使用icc=指定输出色彩空间时，用于RGB响应图像的ICC色彩配置文件的名称。 对于通过各种“图像渲染”命令（例如bgc=和color=）指定的某些RGB颜色值，也是如此。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色配置文件。 指定当未指定输出色彩空间时，用于RGB响应图像的ICC色彩配置文件的名称 `icc=`. 对于通过各种“图像渲染”命令指定的某些RGB颜色值，如 `bgc=` 和 `color=`.

## 属性 {#section-b4a1bd92e99047479a5036413525a6d9}

文本字符串。 如果指定，则必须为有效 `icc::Name` 此材质目录或默认目录的ICC配置文件映射中的值，或相对于 `attribute::RootPath`. 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-5809772f8e96438ab7626d323c66a4ba}

继承自 `default::IccProfileRgb` 如果未定义或为空。

## 另请参阅 {#section-732c17dece3a4575855c9b79a08d0067}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ， [attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)， [attribute：：IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49)， [attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
