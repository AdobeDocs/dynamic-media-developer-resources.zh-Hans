---
description: 將這些伺服器設定用於影像目錄服務。
solution: Experience Manager
title: 影像目錄服務
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# 影像目錄服務{#image-catalog-service}

將這些伺服器設定用於影像目錄服務。

## CS：：catalog.rootPath — 影像目錄資料夾 {#section-02d107f157384b18835f884f24fea3aa}

影像目錄資料夾的位置(全部 [!DNL catalog.ini] 必須找到檔案)。 可以是絕對檔案路徑，也可以是相對於 *[!DNL install_folder]*. 伺服器會持續監控此資料夾，並在新的主要目錄檔案(具有 [!DNL .ini] 檔案字尾)，或現有主要目錄檔案的上次修改時間已變更時偵測到。

## CS：：catalog.cacheRoot — 目錄快取資料夾 {#section-73e499c3a5974f1aa4251e70272ff503}

目錄系統快取的根資料夾。 可設為與中的其中一個資料夾相同 `PS::cache.rootPaths`. 在變更此設定之前，必須手動建立資料夾。

## CS：：catalog.modificationWaitTime — 目錄檔案剖析延遲 {#section-7348065bcc124cb68ea947bf1b9b0845}

目錄服務在之後等待的時間（以毫秒為單位） [!DNL catalog.ini] 檔案會變更，直到載入次要目錄檔案為止。 此延遲有助於確保所有次要目錄檔案在目錄服務嘗試載入之前都是最新的。 以毫秒為單位的整數值。

## CS：：catalog.refreshInterval — 目錄檔案檢查頻率 {#section-517fefc1d8784777a1026abec8630d58}

目錄服務檢查影像目錄變更的頻率。 以毫秒為單位的整數值。
