---
title: init
description: 迴轉檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

迴轉檢視器的JavaScript API參考。

`init()`

啟動迴轉檢視器的初始化。 此時，容器 `DOM` 元素必須建立，好讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分 — 例如，它可能會使用以下專案隱藏 `display:none` style — 檢視器會暫停其初始化程式。 它會暫停，直到網頁將容器元素帶回版面時，檢視器會自動繼續載入。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
