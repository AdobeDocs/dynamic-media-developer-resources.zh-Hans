---
description: 使用這些伺服器設定來設定影像大小限制。
solution: Experience Manager
title: 影像大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 影像大小限制{#image-size-limits}

使用這些伺服器設定來設定影像大小限制。

## IS：：MaxMessageSize — 回應大小限制 {#section-bd942385d4d144cd904003695d72c85e}

限制影像伺服器可傳送至的資料大小 [!DNL Platform Server]. 實際上，這會限制「影像伺服」可透過HTTP (MB)傳回使用者端的編碼/壓縮回應影像的大小。

## IS：：MaxRenderRgnPixels — 輸出影像大小限制 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

限制影像伺服器可產生的影像大小（不包括儲存至檔案的影像）。 大於0的整數值（百萬畫素）。 如果轉譯作業超過大小限制，則會傳回錯誤。 默认值为 16。

## IS：：MaxSavePixels — 儲存至檔案的大小限制 {#section-d1547c4afa88467080ab08356f775e06}

限制影像伺服器將寫入檔案的影像大小 `req=saveToFile` 命令。 大於0的整數值（百萬畫素）。 如果檔案儲存操作超過該限制，則會傳回錯誤。 預設值為1億畫素。

## IS：：MaxNonDsfSize — 非PTIFF輸入影像的大小限制 {#section-50de28a7158a436393cce5da0d1e4d46}

允許影像伺服器開啟的非PTIFF影像大小上限（單位為Mpixels）。 嘗試存取大於此限制的非PTIFF影像時，「影像伺服」會傳回錯誤。

>[!NOTE]
>
>將此值設定得太高可能會造成影像伺服器的記憶體不足，並導致失敗，包括當機。
