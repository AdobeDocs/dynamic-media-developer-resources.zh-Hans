---
description: eCatalog搜尋檢視器支援在主檢視上方呈現影像地圖圖示。
solution: Experience Manager
title: 影像地圖支援
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 影像地圖支援{#image-map-support}

eCatalog搜尋檢視器支援在主檢視上方呈現影像地圖圖示。

對應圖示的外觀會透過CSS控制，如所述 [影像地圖效果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

影像地圖會執行下列三個動作之一：重新導向至外部網頁、「資訊」面板快顯視窗啟用和內部超連結。

## 重新導向至外部網頁 {#section-32ebe3c3a7f74892a428c5d48801de4d}

此 `href` 影像對應的屬性具有外部資源的URL （明確指定，或包裝在其中一個支援的JavaScript範本函式中）： `loadProduct()`， `loadProductCW()`、和 `loadProductPW()`.

以下是簡單URL重新導向的範例：

`href=http://www.adobe.com`

在此範例中，相同的URL會以 `loadProduct()` 函式：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

請注意，當您將JavaScript程式碼新增至 `HREF` 屬性時，程式碼會在使用者端電腦上執行。 因此，請確定JavaScript程式碼是安全的。

## 資訊面板快顯視窗啟用 {#section-7aa036420af646d1ad8cdc388add0b57}

若要使用資訊面板，影像地圖具有 `ROLLOVER_KEY` 屬性集。 此外，設定 `href` 屬性，否則外部URL處理會干擾資訊面板快顯視窗啟動。

最後，請確定檢視器設定包含適當的值 `InfoPanelPopup.template` 以及（選擇性） `InfoPanelPopup.infoServerUrl` 引數。

>[!NOTE]
>
>請注意，當您設定資訊面板快顯視窗時，傳遞至資訊面板的HTML代碼和JavaScript代碼會在使用者端電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 內部超連結 {#section-6afa4fb2fe564c429e0201f019a95849}

按一下影像地圖會在檢視器內執行內部頁面交換。 若要使用該功能，請 `href` 影像地圖中的屬性具有以下特殊格式：

` href=target: *`idx`*`

位置 `*`idx`*` 是目錄跨頁的索引（從零開始）。

以下範例為 `href` 指向eCatalog中3D跨頁的影像地圖屬性：

`href=target:2`
