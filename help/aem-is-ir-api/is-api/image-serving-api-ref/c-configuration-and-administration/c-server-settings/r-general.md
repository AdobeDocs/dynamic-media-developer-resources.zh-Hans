---
description: 一般伺服器設定
solution: Experience Manager
title: 常规
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 常规{#general}

一般伺服器設定

## TC：：PsPort — 主要監聽連線埠 {#section-d31d3051aa994a76b60b70c3d9f7e89f}

指定的主要監聽連線埠 [!DNL Platform Server]. 此連線埠也可用來存取影像伺服、影像演算和Dynamic Media檢視器（如果已安裝）的檔案和範例頁面。

## IS：：CacheServerUrl — 快取服務根Url {#section-bcca227a1f91453b834db4ea050968e2}

指定HTTP根路徑，以允許影像伺服器存取快取服務。 必須設定為 [!DNL http://localhost:TC::PsPort /is/cache/secondary]，且連線埠號碼相符 `TC::PsPort`.

## IS：：RemoteUrlDefaultExpiration — 遠端Image Source預設TTL {#section-e4c31228b459492cacd2f482d9575f71}

透過HTTP從遠端來源取得的快取影像的TTL，使用 `src={…}` 建構。 僅當遠端伺服器的HTTP回應中未包含Expiration標頭時使用。 以秒為單位的整數值。

## IS：：RemoteUrlTimeout — 遠端Image Source逾時 {#section-437646c479cc4bea81dae42100a3c50a}

影像伺服器等待遠端伺服器透過HTTP傳送要求的影像檔案，然後傳回錯誤的時間。 以秒為單位的整數值。

## PS：：allowDefaultCatalogRequests — 啟用/停用預設目錄請求 {#section-484e442a115a49b4ac269d1718b351e1}

設定為false可不允許路徑中未包含有效目錄ID的請求。 默认值为 `true`. 當設定為 `false`，則會針對沒有目錄ID的請求傳回錯誤。

>[!NOTE]
>
>`req=catalogprops` 不受此設定限制。

## PS：：saveToFile.saveTimeout — 檔案儲存逾時 {#section-d22afd8ad86144b28684ed95a59db40e}

的預設逾時值 `req=saveToFile` 時間 `timeout=`未指定。 `msec`. 如果儲存作業未在指定的時間內完成，則會傳回錯誤。
