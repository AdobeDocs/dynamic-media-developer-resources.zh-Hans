---
description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度材料图像的ICC颜色用户档案的名称。
seo-description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度材料图像的ICC颜色用户档案的名称。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度材料图像的ICC颜色用户档案的名称。

## 属性 {#section-97923d8561b845309442d57d017d91a4}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是灰度用户档案。

## 默认 {#section-02c52805ee13483dba7878aeab51f889}

如果未定义或为空，则从`default::IccProfileSrcGray`继承。 如果`attribute::IccProfileSrcGray`未解析为有效用户档案，则将改用`attribute::IccProfileGray`。

## 另请参阅 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，属 [性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，属 [性：:IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
