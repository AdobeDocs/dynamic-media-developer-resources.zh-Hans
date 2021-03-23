---
description: 缩览图分辨率。 指定缩览图图像的对象分辨率。
seo-description: 缩览图分辨率。 指定缩览图图像的对象分辨率。
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---


# ThumbRes{#thumbres}

缩览图分辨率。 指定缩览图图像的对象分辨率。

仅在`catalog::ThumbType=3`时使用。

## 属性 {#section-ee5cae086a3d4875805fa8a08756a586}

实数值大于0。 必须具有与`catalog::Resolution`相同的单位。

## 默认 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` 如果字段不存在，则使用。

## 另请参阅 {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , catalog [::](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)Resolution [, ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501)attribute::ThumbRes [, ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)req=tmb [,  Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
