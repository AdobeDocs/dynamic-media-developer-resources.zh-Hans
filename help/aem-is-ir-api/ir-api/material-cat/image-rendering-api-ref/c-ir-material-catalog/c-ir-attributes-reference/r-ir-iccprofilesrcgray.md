---
description: Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale material images which do not embed a color profile.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度材料图像的ICC颜色配置文件的名称。

## 属性 {#section-97923d8561b845309442d57d017d91a4}

文本字符串。 如果已指定，则必须是有效的 `icc::Name` 此图像目录或默认目录的ICC配置文件映射中的值，或相对于 `attribute::RootPath`. 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-02c52805ee13483dba7878aeab51f889}

Inherited from `default::IccProfileSrcGray` if not defined or if empty. 如果 `attribute::IccProfileSrcGray` 未解析为有效的配置文件， `attribute::IccProfileGray` 的值。

## 另请参阅 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc:：名称](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [属性：:IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
