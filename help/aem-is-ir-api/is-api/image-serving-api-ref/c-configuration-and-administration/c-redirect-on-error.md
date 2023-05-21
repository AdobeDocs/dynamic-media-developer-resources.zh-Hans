---
description: IS伺服器可設定成容錯移轉至替代伺服器，以處理涉及無法成功開啟或讀取之來源影像的要求。
solution: Experience Manager
title: 發生錯誤時重新導向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 發生錯誤時重新導向{#redirect-on-error}

IS伺服器可設定成容錯移轉至替代伺服器，以處理涉及無法成功開啟或讀取之來源影像的要求。

系統會重新導向下列型別的請求：

* IS目錄中的影像，但不在磁碟上。

   如果影像不在目錄中，則在找不到影像時，不應發生錯誤重新導向。

* 損毀的影像、色彩設定檔或字型。
* 磁碟上找不到靜態內容。

   在磁碟上找不到靜態內容請求時，即使參考的靜態內容沒有目錄記錄，也會重新導向靜態內容請求。

錯誤重新導向在任何其他情況下都不會發生。

當啟用並在處理請求期間發生這類錯誤時，主要伺服器會將請求傳送至次要伺服器以進行處理。 然後會直接將回應轉送給使用者端，無論回應是指示成功還是失敗。 主要伺服器會使用快取來標籤此類轉送請求的記錄專案 `REMOTE`. 主要伺服器不會在本機快取回應資料。

錯誤重新導向功能已透過設定啟用 `PS::errorRedirect.rootUrl` 至次要伺服器的HTTP網域名稱和連線埠號碼。 此外，連線逾時設定為 `PS::errorRedirect.connectTimeout` 以及主要伺服器等待次要伺服器回應至使用者端傳回錯誤的最長時間，已設定為 `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>如果無法連絡次要伺服器，則會傳回文字錯誤回應給使用者端，即使已設定預設影像或錯誤影像亦然。

>[!NOTE]
>
>網路路徑中的垂直號字元(|)不支援錯誤重新導向。

## 另请参阅 {#section-2e8bfc128b944baf8108279d16492f3f}

[錯誤重新導向](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
