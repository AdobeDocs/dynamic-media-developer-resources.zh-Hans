---
description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-title: 根路径
solution: Experience Manager
title: 根路径
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# RootPath{#rootpath}

源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。

`RootPath`是文本字符串值。 有关服务器根路径的其他信息，请参见[管理源数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)。

## 属性 {#section-b41d7e0ea63143eb8034569706cad0c0}

文本字符串。 必须为空、有效的相对文件夹路径或图像服务器可以访问的有效绝对路径。

## 默认 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

从`default::RootPath`继承（如果未定义）。 如果已定义但为空，则不会对源文件根路径做出贡献。

## 另请参阅 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [规则集：:PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [管理源数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
