---
description: 偵錯請求。 此偵錯命令會剖析及預先處理請求、執行影像目錄查閱、目錄修飾元包含、巨集和變數替代等，就像req=img一樣。
solution: Experience Manager
title: 解决
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 2%

---

# 解决{#resolve}

偵錯請求。 此偵錯命令會剖析及預先處理請求、執行影像目錄查閱、catalog：：Modifier包含、巨集和變數替代等，就像req=img一樣。

`req=resolve`

傳回的是MIME型別的最終請求字串，而不是結果影像 `text/plain`.

無法快取HTTP回應。
