---
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
title: 處置
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# 處置{#dispose}

eCatalog檢視器的JavaScript API參考。

[!DNL `dispose()`]

釋放檢視器邏輯使用的所有資源，並在執行階段刪除檢視器建立的所有內部物件和元件，以處置此檢視器執行個體。

網頁程式碼也應刪除檢視器例項變數，並從網頁瀏覽器記憶體中完全移除檢視器。

如果網頁程式碼已直接在檢視器使用的Viewer SDK元件上註冊了事件接聽程式，或已儲存此類元件的外部參考，則網頁程式碼必須明確取消註冊此類接聽程式，且呼叫之前必須刪除此類外部元件參考 [!DNL `dispose()`].

之後不再存取Viewer API [!DNL `dispose()`] 稱為。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
