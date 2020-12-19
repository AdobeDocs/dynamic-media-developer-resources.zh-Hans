---
description: 缩略图分辨率。 指定缩略图的对象分辨率。
seo-description: 缩略图分辨率。 指定缩略图的对象分辨率。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# ThumbRes{#thumbres}

缩略图分辨率。 指定缩略图的对象分辨率。

仅在`catalog::ThumbType=3`时使用。

## 属性 {#section-ee5cae086a3d4875805fa8a08756a586}

实数值大于0。 必须具有与`catalog::Resolution`相同的单位。

## 默认 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` 如果字段不存在，则使用该字段（如果值为0或字段为空）。

## 另请参阅 {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [attribute::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) [,缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
