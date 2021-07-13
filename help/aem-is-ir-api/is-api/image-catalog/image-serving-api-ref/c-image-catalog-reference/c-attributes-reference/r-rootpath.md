---
description: 源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootPath{#rootpath}

源数据根路径。 此图像目录源数据的根文件夹的绝对或相对路径。

`RootPath`是一个文本字符串值。 有关服务器根路径的其他信息，请参阅[管理源数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)。

## 属性 {#section-b41d7e0ea63143eb8034569706cad0c0}

文本字符串。 必须为空、有效的相对文件夹路径或图像服务器可访问的有效绝对路径。

## 默认 {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

从`default::RootPath`继承（如果未定义）。 如果定义为空，则不会对源文件根路径产生影响。

## 另请参阅 {#section-6bf4ffc4987843a9a2dbe81b43076437}

[目录：:Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [目录：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
