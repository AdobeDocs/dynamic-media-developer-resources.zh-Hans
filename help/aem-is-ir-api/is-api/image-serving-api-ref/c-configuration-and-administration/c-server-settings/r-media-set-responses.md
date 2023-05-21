---
description: 本節中的設定適用於由req=set修飾元取得的媒體集回應。
solution: Experience Manager
title: 媒體集回應
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 媒體集回應{#media-set-responses}

本節中的設定適用於由req=set修飾元取得的媒體集回應。

## PS：：fvctx.useCatalogRecordValidation — 快取原則 {#section-9accb087d16548a988993bb30395a6f6}

此屬性在決定是否需要重新產生從快取擷取的設定回應時，控制快取原則。 如果屬性停用，則時間戳記會 [!DNL catalog.ini] 檔案用於驗證。 如果已啟用屬性，最新的 `catalog::LastModified` 所有參考記錄中的時間戳記都會用於驗證。

## PS：：fvctx.nestingLimit — 巢狀限制 {#section-280210341f1647fea02590e7069934d2}

任何專案的最大巢狀深度 `req=set` 回應。 如果超過此深度，則會傳回錯誤。

## PS：：fvctx.brochureLimit — 手冊上限 {#section-fe36e47db49244cea7f07e9dd3639440}

中的電子目錄手冊數量上限 `req=set` 包含所有關聯中繼資料的回應。 一旦超過此限制，就會隱藏與手冊專案相關聯的任何私人地圖和使用者資料。
