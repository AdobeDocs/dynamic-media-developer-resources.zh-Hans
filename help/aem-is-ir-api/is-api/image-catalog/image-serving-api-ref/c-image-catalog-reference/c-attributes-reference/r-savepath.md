---
description: saveToFile=的根路徑 將以req=saveToFile產生的影像寫入的根資料夾的相對路徑。
solution: Experience Manager
title: 儲存路徑
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# 儲存路徑{#savepath}

saveToFile=的根路徑 將以req=saveToFile產生的影像寫入的根資料夾的相對路徑。

`SavePath` 是文字字串值。

## 屬性 {#section-343d1371e966491c92854a8df14c3c50}

文字字串。 必須為空白或有效的相對資料夾路徑。 一律與設定的絕對根路徑結合 `ImageServer::SaveDirectory`.

## 默认 {#section-ae751eea97654f399c6aaee3f3252cbb}

繼承自 `default::SavePath` 若未定義。 如果解析的值為空，則會停用儲存至檔案的功能。

## 另请参阅 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
