---
description: 默认缩略图分辨率。 提供缩略图对象分辨率的默认值，以防特定目录记录不包含有效的目录ThumbRes值。
seo-description: 默认缩略图分辨率。 提供缩略图对象分辨率的默认值，以防特定目录记录不包含有效的目录ThumbRes值。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
uuid: 4a77d673-9d2e-4e62-a014-c99fa3df294a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# ThumbRes{#thumbres}

默认缩略图分辨率。 提供缩略图对象分辨率的默认值，以防特定目录记录不包含有效的目录：:ThumbRes值。

仅用于缩略图请求(`req=tmb`)和`catalog::ThumbType=3`时。

## 属性 {#section-88d37d0e030f4879a9e584dd2cc780f3}

实数，大于0。通常以每英寸像素数表示，但也可以以其他单位表示，如每米像素数。

## 默认 {#section-86588899ec9b4276a98b03d7faf64003}

如果未定义或为空，则从`default::ThumbRes`继承。

## 另请参阅 {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
