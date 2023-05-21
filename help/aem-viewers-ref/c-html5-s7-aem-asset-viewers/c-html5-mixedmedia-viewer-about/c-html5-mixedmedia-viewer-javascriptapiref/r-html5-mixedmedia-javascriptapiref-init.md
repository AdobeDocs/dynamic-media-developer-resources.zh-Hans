---
title: init
description: 混合媒體檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

混合媒體檢視器的JavaScript API參考。

`init()`

開始初始化混合媒體檢視器。 此時，必須建立容器DOM元素，好讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分 — 例如，它可能會使用以下專案隱藏 `display:none` style — 檢視器會暫停其初始化程式。 它會暫停，直到網頁將容器元素帶回版面時，檢視器會自動繼續載入。

在檢視器生命週期內只呼叫一次此方法；後續呼叫會被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
