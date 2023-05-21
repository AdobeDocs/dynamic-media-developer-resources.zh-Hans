---
title: 從IS 4.7.4或更新版本更新
description: 在Linux®上升級「Dynamic Media影像伺服」時，請使用此程式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

在Linux®上升級「Dynamic Media影像伺服」時，請使用此程式。

如果您從舊版的「影像伺服」進行升級，請聯絡支援以取得正確的程式。

此 [!DNL webapps] 升級時可刪除資料夾。 請備份 [!DNL webapps] 資料夾（升級前）。

1. 以root許可權登入您的伺服器主機。
1. 解壓縮並解壓縮「影像伺服」發佈tar檔案。
1. 在 [!DNL setup] 資料夾，執行 [!DNL `./install-is`] 以啟動安裝精靈。

   更新安裝程式會檢查已安裝套件的完整性和版本。 如果成功，就會顯示使用者授權合約(「EULA」)。
1. 閱讀授權合約，然後輸入 **[!UICONTROL y]** 以繼續安裝。

   安裝程式會將舊伺服器組態檔備份至 [!DNL BACKUP/] 資料夾。

   安裝完成時，會顯示下列訊息：

   `Image Server was started successfully`

在更新期間， [!DNL ImageServing/conf/server.xml] 檔案已更新至最新設定。 如果您已變更或新增任何值，請儲存現有的 [!DNL server.xml] 並在升級後重新實作變更。

更新安裝後，請考慮先預熱HTTP回應快取，再讓伺服器上線。 請參閱 [!DNL playlog] 公用程式以取得詳細資訊。
