---
description: 默认响应图像。 指定在找不到图像文件且在请求中未指定defaultImage=时要使用的图像或目录条目。
solution: Experience Manager
title: 默认图像
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# 默认图像{#defaultimage}

默认响应图像。 指定在找不到图像文件且在请求中未指定defaultImage=时要使用的图像或目录条目。

可以是目录条目（包括模板）或相对（至`attribute::RootPath`）或绝对图像文件路径。 用于用默认图像替换缺少的图像。

## 属性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文本字符串。 如果指定，则必须是此图像目录中的有效`catalog::Id`值，或者是图像服务器可访问的图像文件的相对（至`attribute::RootPath`）或绝对路径。

## 限制 {#section-5d8ea872f0b0415fbd3a83410bbcf512}

默认图像机制未覆盖外来图像源；如果外来图像源无效，则返回错误。

## 默认 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

如果未定义，则从`default::DefaultImage`继承。 如果已定义但为空，则将禁用默认图像行为，即使定义了`default::DefaultImage`也是如此。

## 另请参阅 {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute：：DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ， [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)，[attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)，[catalog：：Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)，[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)，[attribute：：DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
