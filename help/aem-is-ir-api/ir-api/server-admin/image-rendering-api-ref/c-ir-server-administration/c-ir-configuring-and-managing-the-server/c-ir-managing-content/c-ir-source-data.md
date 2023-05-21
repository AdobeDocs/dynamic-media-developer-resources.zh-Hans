---
description: 影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼花的影像，以及封包和視窗覆蓋樣式檔案）和ICC設定檔。
solution: Experience Manager
title: 來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 來源資料{#source-data}

影像演算來源資料檔案包括暈映檔案、材質檔案（可重複紋理和貼花的影像，以及封包和視窗覆蓋樣式檔案）和ICC設定檔。

所有原始資料檔都必須可供影像演算的原生程式碼元件存取（與影像伺服器共用）。

如果涉及材料目錄，則在材料目錄中指定的檔案(具有 `vignette::Path`， `catalog::Path`，或 `icc::ProfilePath`)會依下列方式由轉譯伺服器查詢：

* 如果路徑是絕對路徑，則會依原樣使用。
* 如果路徑是相對路徑，則會加上前置詞 `catalog::RootPath` （來自已命名的材料目錄）。
* 如果路徑為絕對路徑，則會使用；否則會加上前置詞 `default::RootPath` （來自預設目錄）。
* 如果路徑為絕對路徑，則會加以使用；否則，伺服器會將其與中指定的路徑結合 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* 如果路徑現在是絕對路徑，則會使用；否則，會假設為相對於[！DNL  *[!DNL install_folder]*]。

若未涉及任何影像目錄，則會將路徑與 `default::RootPath` 然後如上處理。

來源資料檔案的實體位置通常會指定 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 可以指定多個值，以允許來源資料檔案散佈到多個檔案系統。 轉譯伺服器會依指定的順序嘗試每個路徑，直到找到資料檔案為止。

任何型別的新資料檔案都可隨時新增，不需停止伺服器。
