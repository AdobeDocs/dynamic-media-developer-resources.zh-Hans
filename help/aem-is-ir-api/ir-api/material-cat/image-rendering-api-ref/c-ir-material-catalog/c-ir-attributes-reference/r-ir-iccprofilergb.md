---
description: RGB默认输出颜色配置文件。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC颜色配置文件的名称，以及使用各种“图像渲染”命令（如bgc=和color=）指定的某些RGB颜色值的名称。
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色配置文件。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC颜色配置文件的名称，以及使用各种“图像渲染”命令（如bgc=和color=）指定的某些RGB颜色值的名称。

## 属性 {#section-b4a1bd92e99047479a5036413525a6d9}

文本字符串。 如果指定，则必须是此材料目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是RGB配置文件。

## 默认 {#section-5809772f8e96438ab7626d323c66a4ba}

从`default::IccProfileRgb`继承（如果未定义或为空）。

## 另请参阅 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [属性：:IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
