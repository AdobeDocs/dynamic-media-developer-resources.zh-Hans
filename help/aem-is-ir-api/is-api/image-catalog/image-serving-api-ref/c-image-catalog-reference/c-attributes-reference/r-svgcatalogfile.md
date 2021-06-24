---
description: SVG数据文件路径。 指定包含此目录的SVG数据的文件。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# SvgCatalogFile{#svgcatalogfile}

SVG数据文件路径。 指定包含此目录的SVG数据的文件。

SVG数据文件在所有图像数据文件之后以指定的确切顺序加载。 如果同一`catalog::Id`值出现在多条记录中（在同一或不同图像或SVG目录文件中），则最后一个实例占上风。

## 属性 {#section-fc2d549f76474792837b2b92ec2087ea}

一个或多个文本字符串值，用逗号分隔。 可选。每个值必须是相对于目录文件夹的绝对文件路径或路径。

## 默认 {#section-a4e58951f3c249599665b823566433c9}

为空，表示此图像目录不包含任何SVG数据。

## 另请参阅 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[目录数据](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)、目 [录文件](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
