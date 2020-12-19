---
description: 默认响应图像。 指定在找不到图像文件且请求中未指定defaultImage=时要使用的图像或目录条目。
seo-description: 默认响应图像。 指定在找不到图像文件且请求中未指定defaultImage=时要使用的图像或目录条目。
seo-title: 默认图像
solution: Experience Manager
title: 默认图像
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8f50af-15bb-4333-b227-3eba38653a7d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

默认响应图像。 指定在找不到图像文件且请求中未指定defaultImage=时要使用的图像或目录条目。

可以是目录条目（包括模板）或相对(`attribute::RootPath`)或绝对图像文件路径。 用默认图像替换缺失的图像非常有用。

## 属性 {#section-b6d8193827c34e5f948792aba8b8daaf}

文本字符串。 如果指定，则必须是此图像目录中有效的`catalog::Id`值，或是图像服务器可访问的图像文件的相对路径(`attribute::RootPath`)或绝对路径。

## 限制{#section-5d8ea872f0b0415fbd3a83410bbcf512}

默认图像机制不覆盖外国图像源；如果外来图像源无效，则返回错误。

## 默认 {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

从`default::DefaultImage`继承（如果未定义）。 如果已定义但为空，则禁用默认图像行为，即使已定义`default::DefaultImage`。

## 另请参阅 {#section-dc0fb4e72294442882b33a479fbc2b82}

[属性：:DefaultImageImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)，属 [性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [Id:IdPatork属性：](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) [ErrorImageImageExpiration属性：:DefaultImageExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
