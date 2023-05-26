---
description: 水印选择器。 指定要用作水印图像或模板的目录记录的目录ID。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# 水印{#watermark}

水印选择器。 指定要用作水印图像或模板的目录记录的catalog：：Id。

如果指定，服务器会将水印应用于所有图像请求的请求图像数据( `req=img`)。

## 属性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文本字符串。 如果指定，则必须为有效 `Catalog::Id` 值(或在默认目录中，如果指定于 [!DNL default.ini])。

## 默认 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

继承自 `default::Watermark` 如果未定义。 如果已定义但为空，则不会对此图像目录应用水印，即使 `default::Watermark` 已定义。

## 另请参阅 {#section-f15dbe31013849828d78588742dde58e}

[catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
