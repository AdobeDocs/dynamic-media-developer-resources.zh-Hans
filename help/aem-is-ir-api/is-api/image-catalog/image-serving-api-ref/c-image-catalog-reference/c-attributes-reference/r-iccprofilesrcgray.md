---
description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种“图像服务”命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。
seo-description: 灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种“图像服务”命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# IccProfileSrcGray{#iccprofilesrcgray}

灰度默认输入颜色用户档案。 指定用于未嵌入颜色用户档案的灰度源图像以及使用各种“图像服务”命令（如color=）指定的特定灰度颜色值的ICC颜色用户档案的名称。

## 属性 {#section-8cbb316df6eb463aaca7b308d3568086}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是灰度用户档案。

## 默认 {#section-bcc7250715884412bd0780f60d1cce7b}

如果未定义或为空，则从`default::IccProfileSrcGray`继承。 如果`attribute::IccProfileSrcGray`未解析为有效用户档案，则使用`attribute::IccProfileGray`。

## 另请参阅 {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
