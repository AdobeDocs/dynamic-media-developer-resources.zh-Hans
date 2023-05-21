---
description: 影像地圖資料。 無或更多完整HTML <area> 元素，由前到後排序。
solution: Experience Manager
title: 地图
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 4%

---

# 地图{#map}

影像地圖資料。 無或更多完整HTML `<AREA>` 元素，由前到後排序。

伺服器將解譯並可能變更SHAPE和COORDS屬性。 （此版本不支援SHAPE=CIRCLE。） 所有其他屬性 `<AREA>` 傳遞而不修改。 使用COORDS屬性指定的座標值必須是未修改來源影像左上角的畫素位移。 (`%` 此版本不支援座標，且可能無法正確處理。)

## 屬性 {#section-f52d89fd399b4356ac05277e6c12f956}

文字字串值。 如果已指定，則必須是一或多個完整的HTML `<AREA>` 元素。

此欄位參與文字字串本地化。 請參閱 [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP通訊協定參考* 以取得詳細資訊。

## 默认 {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

无。

## 另请参阅 {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[對應=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ， [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
