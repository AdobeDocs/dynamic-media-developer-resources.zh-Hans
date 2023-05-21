---
description: 彈出式檢視器的JavaScript API參考。
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# init{#init}

彈出式檢視器的JavaScript API參考。

`init()`

啟動彈出式檢視器的初始化。 此時，必須建立容器DOM元素，好讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分(例如，它可能使用以下專案隱藏： `display:none` 樣式)，檢視器會暫停其初始化程式，直到網頁將容器元素帶回版面配置為止。 發生此情況時，檢視器會自動繼續載入。

在檢視器生命週期中只應呼叫一次此方法，後續的呼叫會被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
