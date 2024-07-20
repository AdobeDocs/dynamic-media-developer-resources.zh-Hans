---
description: 默认缩略图分辨率。 提供特定目录记录中不包含有效目录ThumbRes值时的缩略图对象分辨率默认值。
solution: Experience Manager
title: 缩略图
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# 缩略图{#thumbres}

默认缩略图分辨率。 提供特定目录记录中不包含有效catalog：：ThumbRes值时的缩略图对象分辨率默认值。

仅用于缩略图请求(`req=tmb`)和`catalog::ThumbType=3`时。

## 属性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

实数，大于0。通常以每英寸像素数表示，但也可能以其他单位表示，例如每米像素数。

## 默认 {#section-86588899ec9b4276a98b03d7faf64003}

如果未定义或为空，则从`default::ThumbRes`继承。

## 另请参阅 {#section-a6d2cce2e404441a996dba98a95c8e16}

[目录：：ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
