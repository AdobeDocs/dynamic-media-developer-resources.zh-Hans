---
description: 默认响应图像。 指定在找不到图像文件且未在请求中指定defaultImage=时要使用的图像或目录条目。
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# DefaultImage{#defaultimage}

默认响应图像。 指定在找不到图像文件且未在请求中指定defaultImage=时要使用的图像或目录条目。

可以是目录条目（包括模板）或相对(`attribute::RootPath`)或绝对图像文件路径。 用默认图像替换缺少的图像非常有用。

## 属性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文本字符串。 如果已指定，则必须是此图像目录中的有效`catalog::Id`值，或是图像服务器可访问的图像文件的相对路径（对于`attribute::RootPath`）或绝对路径。

## 限制 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

默认图像机制不覆盖外来图像源；如果外来图像源无效，则返回错误。

## 默认 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

从`default::DefaultImage`继承（如果未定义）。 如果已定义但为空，则会禁用默认图像行为，即使已定义`default::DefaultImage`也是如此。

## 另请参阅 {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
