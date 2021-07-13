---
description: 图像数据文件路径。 指定包含此目录的图像数据的文件。
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---

# CatalogFile{#catalogfile}

图像数据文件路径。 指定包含此目录的图像数据的文件。

图像数据文件按指定的顺序加载。 如果同一`catalog::Id`值出现在多个记录中（在相同或不同的目录文件中），则最后一个实例占上风。

## 属性 {#section-6da55f145ecd4e31a5de52637a436983}

一个或多个文本字符串值，用逗号分隔。 可选。每个值必须是相对于目录文件夹的绝对文件路径或路径。

## 默认 {#section-80f91cd7a6b2479ebb310319e9c74da7}

为空，表示此图像目录不包含任何图像数据。

## 另请参阅 {#section-910b67c5041d44d99a105ad43ff63a37}

[目录数据字段](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
