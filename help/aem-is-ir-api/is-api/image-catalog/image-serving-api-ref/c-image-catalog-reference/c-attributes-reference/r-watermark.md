---
description: 水印选择器。 指定要用作水印图像或模板的目录记录的目录ID。
solution: Experience Manager
title: 水印
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# 水印{#watermark}

水印选择器。 指定用作水印图像或模板的目录记录的catalog::Id。

如果指定，则服务器将水印应用于所有图像请求(`req=img`)的所请求图像数据。

## 属性 {#section-fad6ffff4c5f4b5c8010281bc1377055}

文本字符串。 如果指定，则必须是此图像目录（或默认目录中，如果在[!DNL default.ini]中指定）中的有效`Catalog::Id`值。

## 默认 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

如果未定义，则从`default::Watermark`继承。 如果已定义但为空，则不会为此图像目录应用水印，即使已定义`default::Watermark`。

## 另请参阅 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
