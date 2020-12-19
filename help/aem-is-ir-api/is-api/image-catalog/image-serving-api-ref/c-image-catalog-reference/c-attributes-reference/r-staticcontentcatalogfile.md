---
description: 静态内容目录数据文件路径。 指定包含此目录的静态内容数据的文件。
seo-description: 静态内容目录数据文件路径。 指定包含此目录的静态内容数据的文件。
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

静态内容目录数据文件路径。 指定包含此目录的静态内容数据的文件。

静态内容目录数据文件按指定的顺序加载。 如果同一`static::Id`值出现在多个记录中（在同一或不同的目录文件中），则上一个实例优先。

## 属性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一个或多个文本字符串值，用逗号分隔。 可选。每个值必须是相对于目录文件夹的绝对文件路径或路径。

## 默认 {#section-702edfbc00c54fc29e412a3ff99fef2b}

空，表示此图像目录不包含任何静态内容数据。

## 另请参阅 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目录数据](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
