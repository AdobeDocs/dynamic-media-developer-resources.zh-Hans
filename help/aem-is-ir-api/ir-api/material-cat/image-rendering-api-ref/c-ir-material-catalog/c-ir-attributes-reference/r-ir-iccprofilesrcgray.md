---
title: IccProfileSrcGray
description: 灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度材质图像的ICC颜色配置文件的名称。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
TQID: 'https://experienceleague.adobe.com/j5-F9hrRAYN08NS62Pua7eda-5mlpOOMrdTLIj7Ww6g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度材质图像的ICC颜色配置文件的名称。

## 属性 {#section-97923d8561b845309442d57d017d91a4}

文本字符串。 如果指定，则必须为此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或者相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-02c52805ee13483dba7878aeab51f889}

如果未定义或为空，则从`default::IccProfileSrcGray`继承。 如果`attribute::IccProfileSrcGray`未解析为有效的配置文件，则改用`attribute::IccProfileGray`。

## 另请参阅 {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc：：Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ，[attribute：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[attribute：：IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
