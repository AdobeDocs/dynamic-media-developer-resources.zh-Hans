---
description: 字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。
seo-description: 字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# MetricsPath{#metricspath}

字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。

用于Adobe Type 1字体。 如果未指定，服务器将尝试在主体字体文件所在的同一文件夹中查找字体度量文件。 如果在渲染时找不到所需的字体量度文件，则会出现错误。

## 属性 {#section-955268c581574875b05253d9e14544f3}

文本字符串。 对于Adobe Type 1文件为可选。 必须为空或有效的图像服务器文件路径（绝对或相对于`attribute::RootPath`）。

## 默认 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

无。

## 另请参阅 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
