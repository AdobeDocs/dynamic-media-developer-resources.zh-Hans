---
description: RGB默认输出颜色用户档案。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种"图像渲染"命令（如bgc=和color=）指定的某些RGB颜色值。
seo-description: RGB默认输出颜色用户档案。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种"图像渲染"命令（如bgc=和color=）指定的某些RGB颜色值。
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# IccProfileRgb{#iccprofilergb}

RGB默认输出颜色用户档案。 指定在未使用icc=指定输出色彩空间时用于RGB响应图像的ICC色彩用户档案的名称，以及使用各种&quot;图像渲染&quot;命令（如bgc=和color=）指定的某些RGB颜色值。

## 属性 {#section-b4a1bd92e99047479a5036413525a6d9}

文本字符串。 如果指定，则必须是此材料目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是RGB用户档案。

## 默认 {#section-5809772f8e96438ab7626d323c66a4ba}

如果未定义或为空，则从`default::IccProfileRgb`继承。

## 另请参阅 {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属 [性：:IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
