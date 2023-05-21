---
title: 巢狀請求中的變數處理
description: $var$參考可能出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括「？」的左側 將路徑與查詢分開。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 巢狀請求中的變數處理{#variable-processing-in-nested-requests}

$var$參考可能出現在巢狀影像伺服或影像演算請求的大括弧內的任何位置，包括「？」的左側 將路徑與查詢分開。

伺服器會以（來自url或的）值取代這些參考 `catalog::Modifier` 進一步剖析及處理巢狀要求之前，請先檢查巢狀要求是否存在。

此外，所有 `$ *[!DNL var]*=` url和中的定義 `catalog::Modifier` 轉送至所有巢狀影像伺服和影像演算請求。 這樣做可確保所有變數定義都可供所有範本使用，無論巢狀層級為何。

無論巢狀內嵌層級為何，在巢狀影像演算或影像伺服請求中，只要將單程HTTP編碼套用至變數值，即可在任何地方取代這些值。
