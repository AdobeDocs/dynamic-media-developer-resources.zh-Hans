---
description: 字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# MetricsPath{#metricspath}

字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。

用于Adobe Type1字体。 如果未指定，服务器将尝试在主体字体文件所在的同一文件夹中查找字体量度文件。 如果在渲染时找不到所需的字体量度文件，则会出现错误。

## 属性 {#section-955268c581574875b05253d9e14544f3}

文本字符串。 对于Adobe Type1文件是可选项。 必须为空或有效的图像服务器文件路径（绝对路径或相对于`attribute::RootPath`）。

## 默认 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

无。

## 另请参阅 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
