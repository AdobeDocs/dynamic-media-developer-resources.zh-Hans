---
title: 內嵌外部請求中的變數處理
description: 內嵌外部請求大括弧內任何位置出現的$var$參考會被相符的變數定義值取代。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 內嵌外部請求中的變數處理{#variable-processing-in-embedded-foreign-requests}

任何 `$var$` 內嵌外部請求大括弧內任何位置發生的參考，會以相符的變數定義值取代。

允許將內嵌的外部請求放置在影像目錄的範本中。

要取代成外部請求的變數值通常必須經過雙重編碼，因為在伺服器嘗試傳輸最終的外部URL之前，不會套用重新編碼。
