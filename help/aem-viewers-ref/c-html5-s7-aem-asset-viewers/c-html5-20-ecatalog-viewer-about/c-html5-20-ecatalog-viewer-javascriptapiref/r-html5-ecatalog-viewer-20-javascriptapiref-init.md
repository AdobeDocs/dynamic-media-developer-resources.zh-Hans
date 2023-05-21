---
title: init
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e7775a65-67bf-4ad6-8e51-1fdf141946bc
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 2%

---

# init{#init}

eCatalog檢視器的JavaScript API參考。

`init()`

啟動eCatalog檢視器的初始化。 此時必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分 — 例如，它可能會使用以下專案隱藏 `display:none` 樣式已指定給檢視器 — 檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

在檢視器生命週期內只呼叫一次此方法；後續呼叫會被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
\<instance>.init()
```
