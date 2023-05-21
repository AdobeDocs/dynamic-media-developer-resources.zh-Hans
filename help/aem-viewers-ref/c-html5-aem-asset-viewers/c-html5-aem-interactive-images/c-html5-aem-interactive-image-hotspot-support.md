---
title: 熱點支援
description: 熱點支援
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 熱點支援{#hotspot-support}

檢視器支援在主檢視上方呈現熱點圖示。 熱點圖示的外觀會透過CSS控制，如熱點區段中所述。

另請參閱 [熱點](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

連結區可以觸發JavaScript回呼，藉此在託管網頁上啟用「快速檢視」功能，或將使用者重新導向至外部網頁。

## 快速檢視熱點 {#section-cda48fc9730142d0bb3326bac7df3271}

這些型別的熱點應使用Dynamic Media中的「快速檢視」動作型別(即Adobe Experience Manager Assets — 隨選)來編寫。 當使用者啟動此類熱點時，檢視器會執行 `quickViewActivate` JavaScript回呼並將熱點資料傳遞給它。 內嵌網頁應會監聽此回呼。 觸發頁面時，會開啟自己的快速檢視實施。

## 重新導向至外部網頁 {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience Manager Assets的Dynamic Media中為「快速檢視」動作型別製作的熱點 — 隨選將使用者重新導向至外部URL。 根據編寫期間所做的設定，URL會在新的瀏覽器標籤中、同一視窗中或在指定的瀏覽器視窗中開啟。
