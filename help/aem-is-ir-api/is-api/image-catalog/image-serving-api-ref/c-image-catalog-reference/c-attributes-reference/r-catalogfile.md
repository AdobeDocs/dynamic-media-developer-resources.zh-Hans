---
description: 图像数据文件路径。 指定包含此目录的图像数据的文件。
solution: Experience Manager
title: 目录文件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 3%

---

# 目录文件{#catalogfile}

图像数据文件路径。 指定包含此目录的图像数据的文件。

图像数据文件将按指定的顺序加载。 如果同一个`catalog::Id`值出现在多个记录中（在同一目录文件中或不同目录文件中），则最后一个实例优先。

## 属性 {#section-6da55f145ecd4e31a5de52637a436983}

一个或多个文本字符串值，用逗号分隔。 可选. 每个值都必须是绝对文件路径或相对于目录文件夹的路径。

## 默认 {#section-80f91cd7a6b2479ebb310319e9c74da7}

为空，这表示此图像目录不包含任何图像数据。

## 另请参阅 {#section-910b67c5041d44d99a105ad43ff63a37}

[目录数据字段](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
