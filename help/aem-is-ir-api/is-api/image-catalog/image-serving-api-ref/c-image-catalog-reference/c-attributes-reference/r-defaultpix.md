---
description: 默认视图大小。
solution: Experience Manager
title: Defaultpix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Defaultpix{#defaultpix}

默认视图大小。

如果请求未明确使用指定视图大小，服务器将限制回复图像不超过此宽度和高度 `wid=`， `hei=`，或 `scl=`.

## 属性 {#section-c3e658cf82c540d986b118f74f0fe1b2}

0或更大的两个整数，以逗号分隔。 宽度和高度（像素）。 可以将任一值或两个值都设置为0以保持其不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-b7338b2bf5114fff83b0714a57b20639}

继承自 `default::DefaultPix` 如果未定义或为空。

## 另请参阅 {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [catalog：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
