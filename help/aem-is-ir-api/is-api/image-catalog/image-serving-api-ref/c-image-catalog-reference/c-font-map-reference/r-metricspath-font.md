---
description: 字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。
solution: Experience Manager
title: 量度路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 3%

---

# 量度路径{#metricspath}

字体量度文件路径。 字体量度文件的路径和名称，包括文件后缀。

用于Adobe Type 1字体。 如果未指定，则服务器将尝试在主体字体文件所在的同一文件夹中找到字体度量文件。 如果在渲染时找不到所需的字体量度文件，则会发生错误。

## 属性 {#section-955268c581574875b05253d9e14544f3}

文本字符串。 对于Adobe Type 1文件为可选。 必须为空或有效的图像服务器文件路径，可以是绝对路径或相对于`attribute::RootPath`的路径。

## 默认 {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

无。

## 另请参阅 {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[属性：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
