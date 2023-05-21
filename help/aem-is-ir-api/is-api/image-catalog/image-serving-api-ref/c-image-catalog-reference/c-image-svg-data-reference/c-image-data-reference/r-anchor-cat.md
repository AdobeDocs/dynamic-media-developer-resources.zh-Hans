---
description: 影像錨點。 此影像作為範本或複合影像中的圖層時的原點。
solution: Experience Manager
title: 锚点
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# 锚点{#anchor}

影像錨點。 此影像作為範本或複合影像中的圖層時的原點。

也會定義預設的旋轉中心點。

## 屬性 {#section-95740f14160744e7bc763094b8be40d8}

以逗號分隔的兩個整數。 相對於全解析度影像左上角的畫素位移。

覆寫者 `anchor=`(接著可覆寫為 `origin=`)。

## 默认 {#section-ca3a4cc837d643519eff15951f2b47a1}

如果此欄位不存在或空白，且這是有效的影像記錄(亦即 `catalog::Path` 為有效)。

## 另请参阅 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ， [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
