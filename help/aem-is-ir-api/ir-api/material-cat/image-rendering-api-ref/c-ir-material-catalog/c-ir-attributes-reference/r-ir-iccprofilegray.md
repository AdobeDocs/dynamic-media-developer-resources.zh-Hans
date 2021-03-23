---
description: 灰度默认色彩空间。 指定在未指定icc=输出色彩空间时用于灰度响应图像的ICC色彩用户档案的名称。
seo-description: 灰度默认色彩空间。 指定在未指定icc=输出色彩空间时用于灰度响应图像的ICC色彩用户档案的名称。
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
uuid: 064be242-d964-4fb8-99ea-78bb5599e70f
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

灰度默认色彩空间。 指定在未指定icc=输出色彩空间时用于灰度响应图像的ICC色彩用户档案的名称。

## 属性 {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

文本字符串。 如果指定，则必须是此材料目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是灰度用户档案。

## 默认 {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

如果未定义或为空，则从`default::IccProfileGray`继承。

## 另请参阅 {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属 [性：:IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
