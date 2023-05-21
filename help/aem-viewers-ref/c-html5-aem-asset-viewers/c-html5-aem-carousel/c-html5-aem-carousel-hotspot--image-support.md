---
title: 熱點和影像地圖支援
description: 熱點和影像地圖支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 熱點和影像地圖支援{#hotspot-and-image-maps-support}

檢視器支援在主檢視上方呈現熱點圖示和影像地圖區域。 熱點圖示和區域的外觀會透過CSS控制，如自訂熱點和影像地圖區段中所述。

另請參閱 [連結區和影像地圖](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

熱點和區域可以觸發JavaScript回呼，在託管網頁上啟用「快速檢視」功能，或將使用者重新導向至外部網頁。

## 快速檢視熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些型別的熱點或影像地圖應使用Adobe Experience Manager的Dynamic Media中的「快速檢視」動作型別編寫。 當使用者啟動此類熱點或影像地圖時，檢視器會執行 `quickViewActivate` JavaScript回呼並將熱點或影像地圖資料傳遞至該回呼。 內嵌網頁應會監聽此回呼。 觸發頁面時，會開啟自己的快速檢視實施。

## 重新導向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

為Experience Manager的Dynamic Media中的動作型別「快速檢視」製作的熱點或影像地圖，會將使用者重新導向至外部URL。 根據編寫期間所做的設定，URL會在新的瀏覽器標籤中、同一視窗中或在指定的瀏覽器視窗中開啟。
