---
title: init
description: Video Viewer的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9e83b773-c059-45c6-a249-ef0ed2799a05
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# init{#init}

Video Viewer的JavaScript API參考。

`init()`

開始初始化Video Viewer。 此時，必須建立容器DOM元素，好讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分(例如，它可能使用以下專案隱藏： `display:none` 樣式)，檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 進行此程式時，檢視器載入會自動繼續。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
