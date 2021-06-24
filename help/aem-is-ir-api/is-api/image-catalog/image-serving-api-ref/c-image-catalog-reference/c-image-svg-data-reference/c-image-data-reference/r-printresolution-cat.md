---
description: 打印分辨率。 打印全尺寸图像的分辨率。
solution: Experience Manager
title: 打印分辨率
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 2168d72a-1f2b-4833-9e6e-ba3d2ddb6d2b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---

# 打印分辨率{#printresolution}

打印分辨率。 打印全尺寸图像的分辨率。

该值会嵌入在回复图像标头中，除非用`printRes=`来覆盖。

## 属性 {#section-de3c1f73da7b43208beeec841c1778c1}

整数，大于0。 以每英寸点数表示。 可选。

## 默认 {#section-0cac992554ec4247ab05f70d9840a045}

`attribute::PrintResolution` 如果字段不存在，则当值为0或字段为空时，将使用。

## 另请参阅 {#section-0593faefffe341c5ab8a4aa5da589a04}

[attribute::PrintResolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-printresolution.md#reference-a53c6850077148c9bd88a8c5c1c400c5) ,  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [printRes=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491)
