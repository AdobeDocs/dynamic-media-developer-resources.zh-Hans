---
description: 灰度默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于灰度响应图像的ICC色彩用户档案的名称，以及使用各种“图像服务”命令（如color=）指定的特定灰度颜色值。
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

灰度默认输出颜色用户档案。 指定当没有使用icc=指定输出色彩空间时用于灰度响应图像的ICC色彩用户档案的名称，以及使用各种“图像服务”命令（如color=）指定的特定灰度颜色值。

## 属性 {#section-03f090ee2acf4537b83f78840d23ecab}

文本字符串。 如果指定，则必须是此图像目录或默认目录的ICC用户档案映射中的有效`icc::Name`值，或是相对于`attribute::RootPath`的文件路径。 引用的ICC用户档案必须是灰度用户档案。

## 默认 {#section-95ba3ab15edc4259b657c6ebf8783d61}

如果未定义或为空，则从`default::IccProfileGray`继承。

## 另请参阅 {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ，属 [性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
