---
description: 使用這些伺服器設定來偵錯追蹤記錄。
solution: Experience Manager
title: Debug_trace記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---

# Debug_trace記錄{#debug-trace-logging}

使用這些伺服器設定來偵錯追蹤記錄。

>[!NOTE]
>
>建議將所有記錄檔設定為寫入相同的資料夾 `TC::directory`. 這可確保所有「影像伺服」記錄檔都參與設定的自動記錄檔旋轉 `TC::maxDays`，可防止因磁碟空間不足狀況而造成伺服器不穩定。

## SV：：log — 伺服器監督員追蹤記錄檔路徑 {#section-3697bc480ff646e79cacc2812c55ef26}

伺服器管理員記錄檔的資料夾和基本檔案名稱。 路徑可以是絕對或相對於 *[!DNL install_folder]*. Server Supervisor將會附加連字型大小以及目前的日期( *[!DNL -yyyy-mm-dd]*)至檔案名稱(在檔案字尾之前（如果有的話）。 建議將所有記錄檔傳送至與相同的資料夾 [!DNL Platform Server] 記錄檔( `PS::LogFolder`)以運用由實作的記錄檔管理 [!DNL Platform Server] ( `PS::LogDays`)。 默认值为 [!DNL logs/Supervisor.log].

>[!NOTE]
>
>在變更此設定之前，必須先建立新資料夾。 請確定存取許可權已設定，以便Server Supervisor擁有必要的建立、讀取和寫入許可權。

## SV：：tracelevel — 伺服器監督員追蹤記錄層級 {#section-36f8634741da4c618d67aa628b5fe474}

記錄層級可以是1、2、3或4。 默认值为 2。

## IS：：Log — 影像伺服器偵錯記錄檔路徑 {#section-73a3f09b77f2446c9f82207b7d8aec39}

影像伺服器追蹤記錄檔的資料夾和基本檔案名稱。 路徑可以是絕對或相對於 *[!DNL install_folder]*. ImageServer會附加連字型大小與目前日期( *[!DNL -yyyy-mm-dd]*)至檔案名稱(在檔案字尾之前（如果有的話）。 建議將影像伺服器記錄檔傳送至與相同的資料夾 [!DNL Platform Server] 記錄檔( `PS::LogFolder`)以運用由實作的記錄檔管理 [!DNL Platform Server] (請參閱 `PS::LogDays`)。

>[!NOTE]
>
>在變更此設定之前，必須先建立新資料夾。 請確定存取許可權已設定，讓「影像伺服」具備必要的建立、讀取和寫入許可權。

## IS：TraceClient — 影像伺服器偵錯記錄層級 {#section-3851f1f68e404430985c629ac80534db}

記錄層級可以是1、2、3或4 （預設為2）

層級1會記錄與啟動、關閉和關閉相關的事件 [!DNL Platform Server] 連線。

層級2也會記錄來源影像的連線與中斷連線。

第3級新增畫素資料請求的記錄及傳送至 [!DNL Platform Server].

層級4會記錄從 [!DNL Platform Server].

層級3和4應僅用於偵錯，因為記錄檔可能會變得非常大。

## IS：：TraceStatsInterval — 影像伺服器統計資料記錄間隔 {#section-1d8df96d61044e33a5b2b2b0309c2d59}

影像伺服器會以此設定指定的間隔，將記憶體統計資料寫入其追蹤記錄檔。 有效範圍為5到86,400秒。
