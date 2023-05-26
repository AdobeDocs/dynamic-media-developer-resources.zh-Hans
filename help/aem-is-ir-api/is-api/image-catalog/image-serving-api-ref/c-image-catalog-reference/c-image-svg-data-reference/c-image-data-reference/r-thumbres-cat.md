---
description: 缩略图分辨率。 指定缩略图图像的对象分辨率。
solution: Experience Manager
title: 缩略图
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# 缩略图{#thumbres}

缩略图分辨率。 指定缩略图图像的对象分辨率。

仅在以下情况下使用 `catalog::ThumbType=3`.

## 属性 {#section-ee5cae086a3d4875805fa8a08756a586}

大于0的实数值。 必须具有与相同的单位 `catalog::Resolution`.

## 默认 {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` 如果字段不存在、值为0或字段为空，则使用。

## 另请参阅 {#section-eb716bf647614db083020fe8ce453751}

[目录：ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ， [catalog：：Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)， [attribute：：ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501)， [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
