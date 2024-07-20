---
description: 数据文件路径SVG。 指定包含此目录的SVG数据的文件。
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# SvgCatalogFile{#svgcatalogfile}

数据文件路径SVG。 指定包含此目录的SVG数据的文件。

SVG数据文件将按照指定的确切顺序加载到所有图像数据文件之后。 如果同一个`catalog::Id`值出现在多个记录中(在同一或不同的图像或SVG目录文件中)，则最后一个实例将优先。

## 属性 {#section-fc2d549f76474792837b2b92ec2087ea}

一个或多个文本字符串值，用逗号分隔。 可选。 每个值都必须是绝对文件路径或相对于目录文件夹的路径。

## 默认 {#section-a4e58951f3c249599665b823566433c9}

为空，这表示此图像目录不包含任何SVG数据。

## 另请参阅 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[目录数据](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)，[目录文件](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
