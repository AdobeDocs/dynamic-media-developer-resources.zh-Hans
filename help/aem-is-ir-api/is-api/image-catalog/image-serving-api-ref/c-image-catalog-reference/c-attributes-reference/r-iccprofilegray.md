---
title: Icc配置文件灰色
description: 灰度默认输出颜色配置文件。 指定当没有使用icc=指定输出颜色空间时，用于灰度响应图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的名称。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# Icc配置文件灰色{#iccprofilegray}

灰度默认输出颜色配置文件。 指定当没有使用icc=指定输出颜色空间时，用于灰度响应图像的ICC颜色配置文件的名称，以及用于使用各种“图像提供”命令（例如color=）指定的某些灰度颜色值的名称。

## 属性 {#section-03f090ee2acf4537b83f78840d23ecab}

文本字符串。 如果指定，则必须为有效 `icc::Name` 值，该值来自此图像目录或默认目录的ICC配置文件映射，或相对于该图像目录的文件路径 `attribute::RootPath`. 引用的ICC配置文件必须是灰度配置文件。

## 默认 {#section-95ba3ab15edc4259b657c6ebf8783d61}

继承自 `default::IccProfileGray` 如果未定义或为空。

## 另请参阅 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc：：Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [属性：：IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
