---
description: 此發行版本（Image Serving 6.6.1和Image Rendering 6.6.1）取代Image Serving 6.5.3和Image Rendering 6.5.3。
solution: Experience Manager
title: 關於此版本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---

# 關於此版本{#about-this-release}

此發行版本（Image Serving 6.6.1和Image Rendering 6.6.1）取代Image Serving 6.5.3和Image Rendering 6.5.3。

## 已知問題和行為變更 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支援在資產ID中使用問號字元，即使該字元為URL編碼亦然。
* 動態橫幅 `/xfl/flash/` 不再支援要求，現在傳回http 404錯誤代碼。
* W2P `/is/agm/` 不再支援要求。
* 部分錯誤訊息不再呈現至瀏覽器。 因此，您需要檢閱追蹤記錄以進行偵錯。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智慧型色票
* 智慧型裁切

## 錯誤修正 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 已修正以下問題： `\qc` RTF選項後跟空格導致請求無法呈現。
