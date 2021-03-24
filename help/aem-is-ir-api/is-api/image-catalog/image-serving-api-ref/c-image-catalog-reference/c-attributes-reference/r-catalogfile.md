---
description: 图像数据文件路径。 指定包含此目录的图像数据的文件。
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

图像数据文件路径。 指定包含此目录的图像数据的文件。

图像数据文件按指定的顺序加载。 如果多条记录（在同一或不同的目录文件中）中出现相同的`catalog::Id`值，则最后一个实例优先。

## 属性 {#section-6da55f145ecd4e31a5de52637a436983}

一个或多个文本字符串值，用逗号分隔。 可选。每个值必须是相对于目录文件夹的绝对文件路径或路径。

## 默认 {#section-80f91cd7a6b2479ebb310319e9c74da7}

空，表示此图像目录不包含任何图像数据。

## 另请参阅 {#section-910b67c5041d44d99a105ad43ff63a37}

[目录数据字段](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
