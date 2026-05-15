---
description: 静态内容目录数据文件路径。 指定包含此目录的静态内容数据的文件。
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# StaticContentCatalogFile{#staticcontentcatalogfile}

静态内容目录数据文件路径。 指定包含此目录的静态内容数据的文件。

按指定的顺序加载静态内容目录数据文件。 如果同一个`static::Id`值出现在多个记录中（在同一目录文件中或不同目录文件中），则最后一个实例优先。

## 属性 {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

一个或多个文本字符串值，用逗号分隔。 可选. 每个值都必须是绝对文件路径或相对于目录文件夹的路径。

## 默认 {#section-702edfbc00c54fc29e412a3ff99fef2b}

为空，这表示此图像目录不包含任何静态内容数据。

## 另请参阅 {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[目录数据](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
