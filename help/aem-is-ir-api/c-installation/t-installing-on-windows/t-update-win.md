---
title: 從IS 4.7.4或更新版本更新
description: 升級Dynamic Media影像伺服時請使用此程式。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 從IS 4.7.4或更新版本更新{#updating-from-is-or-later}

升級Dynamic Media影像伺服時請使用此程式。

如果您從舊版的「影像伺服」進行升級，請聯絡支援以取得正確的程式。

>[!NOTE]
>
>此 [!DNL webapps] 升級時可能會刪除資料夾。 備份 [!DNL webapps] 資料夾（升級前）。

1. 以管理許可權登入您的伺服器主機。
1. 解壓縮「影像伺服」發佈zip檔案的內容。
1. 執行以啟動安裝精靈 `setup/setup.exe`.
1. 選取 **[!UICONTROL 下一個]** 若要前進到使用者授權合約(EULA)，請閱讀授權合約，然後選取 **[!UICONTROL 是]**.

   下一頁顯示先前的組態設定。
1. 按一下 **[!UICONTROL 下一個]** 以開始更新安裝。

   >[!NOTE]
   >
   >安裝程式會將舊伺服器組態檔備份至 [!DNL BACKUP/] 資料夾。

1. 安裝完成後，請選取 **[!UICONTROL 完成]** 以結束安裝精靈。

   有時安裝精靈可能會要求您重新開機。

在更新期間， [!DNL ImageServing/conf/server.xml] 檔案已更新至最新設定。 如果您已變更或新增任何值，則應儲存現有的 [!DNL server.xml] 並在升級後重新實作變更。

更新安裝後，請考慮先預熱HTTP回應快取，再讓伺服器上線。 請參閱 `playlog` 公用程式以取得詳細資訊。
