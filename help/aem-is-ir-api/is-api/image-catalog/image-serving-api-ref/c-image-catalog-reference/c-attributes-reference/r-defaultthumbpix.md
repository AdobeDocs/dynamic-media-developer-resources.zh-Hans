---
description: 默认缩略图大小。 用于替代缩略图请求(req=tmb)的属性DefaultPix。
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

默认缩略图大小。 用于缩略图请求(req=tmb)，而不是attribute：：DefaultPix。

如果缩略图请求( `req=tmb`)不会明确指定大小，也不会明确使用以下选项指定视图大小： `wid=`， `hei=`，或 `scl=`.

## 属性 {#section-650d9b1194fb4c47a03c6809e6b4af0e}

0或更大的两个整数，以逗号分隔。 宽度和高度（像素）。 可以将任一值或两个值都设置为0以保持其不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-2c4a4f14540449638822913513170ff1}

继承自 `default::DefaultThumbPix` 如果未定义或为空。

## 另请参阅 {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
