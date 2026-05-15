---
description: 灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度源图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的ICC颜色配置文件的名称。
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
TQID: 'https://experienceleague.adobe.com/T6hvJ0NuHHHN3io1u0BbkQMbaIZEPXpwZJddf-VR7So'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 1%

---

# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色配置文件。 指定用于未嵌入颜色配置文件的灰度源图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的ICC颜色配置文件的名称。

## 属性 {#section-8cbb316df6eb463aaca7b308d3568086}

文本字符串。 如果指定，则必须为此图像目录或默认目录的ICC配置文件映射中的有效`icc::Name`值，或者相对于`attribute::RootPath`的文件路径。 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-bcc7250715884412bd0780f60d1cce7b}

如果未定义或为空，则从`default::IccProfileSrcGray`继承。 如果`attribute::IccProfileSrcGray`未解析为有效的配置文件，则改用`attribute::IccProfileGray`。

## 另请参阅 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)，[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
