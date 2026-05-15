---
description: 水印选择器。 指定要用作水印图像或模板的目录记录的目录ID。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 2%

---

# 水印{#watermark}

水印选择器。 指定要用作水印图像或模板的目录记录的catalog：：Id。

如果指定，服务器会将水印应用于所有图像请求( `req=img`)的所请求图像数据。

## 属性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文本字符串。 如果指定，则必须为此图像目录中（或默认目录中，如果在[!DNL default.ini]中指定）的有效`Catalog::Id`值。

## 默认 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

如果未定义，则从`default::Watermark`继承。 如果已定义但为空，则即使定义了`default::Watermark`，也不会对此图像目录应用水印。

## 另请参阅 {#section-f15dbe31013849828d78588742dde58e}

[catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
