---
description: SVG数据文件路径。 指定包含此目录的SVG数据的文件。
seo-description: SVG数据文件路径。 指定包含此目录的SVG数据的文件。
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 3%

---


# SvgCatalogFile{#svgcatalogfile}

SVG数据文件路径。 指定包含此目录的SVG数据的文件。

SVG数据文件在以指定的精确顺序加载所有图像数据文件之后。 如果多条记录（在同一或不同图像或SVG目录文件中）中出现相同的`catalog::Id`值，则最后一个实例优先。

## 属性 {#section-fc2d549f76474792837b2b92ec2087ea}

一个或多个文本字符串值，用逗号分隔。 可选。每个值必须是相对于目录文件夹的绝对文件路径或路径。

## 默认 {#section-a4e58951f3c249599665b823566433c9}

空，表示此图像目录不包含任何SVG数据。

## 另请参阅 {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Catalog Data](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29),  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
