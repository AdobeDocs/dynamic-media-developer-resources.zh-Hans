---
title: 相容性說明
description: 作業系統、瀏覽器和行動裝置的相容性注意事項。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7ad499b1-7da6-483b-ab11-cff2eb9271da
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 1%

---

# 相容性說明{#compatibility-notes}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

作業系統、瀏覽器和行動裝置的相容性注意事項。

## BlackBerry® {#section-0c465ac3775d47fd838e2695a00abc45}

* 與舊版最適化視訊集不相容。 重新上傳最適化視訊集以允許播放。

## 常规 {#section-7b9a9fcba85148d1802b7b3016b48e02}

* 瀏覽器端縮放會造成UI和影像在使用者放大至頁面時變得模糊。 使用者介面格式也會根據縮放顯示不正確，並會延續到全熒幕。
* 由於行動裝置上的大小限制，混合媒體檢視器會使用滑動手勢來交換內嵌影像集中的影格，而非點選內嵌色票元件。 元件以視覺指示器的形式存在。
* 在Internet Explorer瀏覽器和某些觸控裝置中，全熒幕模式不會佔據整個裝置熒幕。 而是將應用程式的大小調整為瀏覽器視窗的大小。
* 「關閉」按鈕在iOS 8.0和iOS 8.1下無法運作，但可在iOS 8.2下運作。

## Galaxy SIII {#section-dfd5f46f39834223b544b1e2f7a770c1}

* 使用Zoom和eCatalog檢視器時發現記憶體流失。 重複瀏覽畫面會導致瀏覽器當機。
* 在檢視器上點兩下會導致整個頁面縮放，而非只縮放已啟用瀏覽器端縮小的檢視器。

## Galaxy S4 {#section-7effabfea75b488399e0f71cab4ce76b}

* 在直向模式中偵測到裝置為平板電腦，且瀏覽器設定中勾選全熒幕。

## Galaxy Nexus {#section-9340b0b026bd48e8a8a6b837b59c6dc5}

* 在檢視器上點兩下會導致整個頁面縮放，而不僅僅是檢視器，並啟用瀏覽器端縮放。

## Galaxy Nexus 10和Galaxy平板電腦 {#section-ef52bd1249fe4f358c11838f7a557a00}

* eCatalog以直向和橫向顯示不正確的頁面跨頁。

## HTC行動裝置 {#section-dc42c80414c842e488738fc157c55b01}

* 無法停用原生縮放，這是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「捏合縮放」手勢時，此功能可導致整個頁面縮放。 請改用點兩下手勢。
* 如果影像地圖很小且很接近，則影像地圖圖示會重疊。

## HTML5視訊檢視器 {#section-3c2dd1220dea4093b17ca2dd0a688307}

* `IntialBitRate` 修飾元僅支援軟體HLS和FlashHDS播放。 使用原生播放器播放時無法運作。
* 不支援OGG和WebM漸進式播放。
* 瀏覽器縮放導致視訊播放器顯示大小不正確(包括Windows®控制面板顯示設定)。
* 在Safari上使用HLS串流的視訊搜尋不一致。

## Internet Explorer {#section-a18e8df396954f0b807017787c00aac7}

* 不支援Quirks模式。
* 不支援相容性模式。
* 不支援行動裝置上的Internet Explorer。

## iOS {#section-70161cba8c2044838d916d0b69c12247}

* 大型eCatalog會導致瀏覽器在iPad 2上當機。

## Safari {#section-f8de598293d349188aa02c82cd3af8b6}

* Safari 6.1或更新版本：網際網路外掛程式設定會防止Flash視訊播放。
* 在Safari上使用HLS串流的視訊搜尋不一致。
* 無法使用HLS串流在Safari 6上搜尋視訊結尾。
