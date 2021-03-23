---
description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
seo-title: RootPath
solution: Experience Manager
title: RootPath
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# RootPath{#rootpath}

源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。

`RootPath`是文本字符串值。 有关服务器根路径的其他信息，请参见[管理源数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)。

## 属性 {#section-b41d7e0ea63143eb8034569706cad0c0}

文本字符串。 必须为空、有效的相对文件夹路径或图像服务器可以访问的有效绝对路径。

## 默认 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

如果未定义，则从`default::RootPath`继承。 如果已定义但为空，则不会向源文件根路径贡献。

## 另请参阅 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , catalog [::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)MaskPath  [, ruleset](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)::PathRule [, Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
