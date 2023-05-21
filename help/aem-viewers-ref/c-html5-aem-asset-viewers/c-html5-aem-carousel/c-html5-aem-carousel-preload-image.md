---
title: 預先載入影像
description: 預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的用途是在視覺上改善檢視器載入時間，並快速將內容呈現給使用者。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 預先載入影像{#preload-image}

預先載入影像是靜態資產預覽影像，在呼叫init()方法後立即載入，並在下載檢視器SDK程式庫、資產和預設集資訊時顯示。 預先載入影像的用途是在視覺上改善檢視器載入時間，並快速將內容呈現給使用者。

預先載入影像適用於最常見的檢視器內嵌方法，也就是不受高度限制的回應式內嵌。 檢視標題 [高度不受限制的回應式設計內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

但是，當使用其他內嵌方法或特定設定選項時，功能會有某些限制。 在下列情況下，預先載入影像可能無法正確轉譯：

* 如果檢視器的大小固定，且大小是使用以下其中一種來定義 `stagesize` 檢視器預設集記錄內的設定屬性，或頂層檢視器容器元素的外部檢視器CSS檔案內的設定屬性。
* 使用彈性大小內嵌，且使用定義寬度與高度的檢視器內嵌方法時。 檢視標題 [定義寬度和高度的彈性大小內嵌](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

如果您在上面列出的操作模式之一中使用檢視器，請使用來停用預先載入影像功能。 `preloadImage` 設定屬性。

此外，即使已在設定中啟用，也不會使用預先載入影像，前提是檢視器已嵌入至DOM元素，並使用進行隱藏 `display:none` CSS設定，或從DOM樹狀結構中斷連結。
