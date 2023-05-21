---
title: 解析模式
description: 重新取樣模式。 resMode=的預設值。 指定用來將演算後的影像縮放至最終大小的重新取樣和插值屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c57932a0-529c-4f31-b60e-a38de6fe277f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---

# 解析模式{#resmode}

重新取樣模式。 的預設值 `resMode=`. 指定用來將演算後的影像縮放至最終大小的重新取樣和插值屬性。

## 屬性 {#section-1183a155f33c4eca80f1dc6fb6bda1b5}

列舉。 設為2 `'bilin'`， 3表示 `'bicub'`，或4個 `'sharp2'` 內插模式(請參閱 [resMode=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md) 以取得詳細資訊)。

## 默认 {#section-ed432a0acc3e4bce926a07e9cfd2c865}

繼承自 `default::ResMode` 如果未定義或為空。

## 另请参阅 {#section-34b71c295b4349dfb4379823a2de83c2}

[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
