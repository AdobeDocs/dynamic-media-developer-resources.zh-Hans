---
description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-title: RootPath
solution: Experience Manager
title: RootPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# RootPath{#rootpath}

源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。

是 `RootPath` 一个文本字符串值。 有关服 [务器根路径的其他信息](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) ，请参阅管理源数据。

## 属性 {#section-b41d7e0ea63143eb8034569706cad0c0}

文本字符串。 必须为空、有效的相对文件夹路径或图像服务器可以访问的有效绝对路径。

## 默认 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

如果未定义， `default::RootPath` 则从中继承。 如果已定义但为空，则不会贡献到源文件根路径。

## 另请参阅 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), ruleset::PathRule [,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)[Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
