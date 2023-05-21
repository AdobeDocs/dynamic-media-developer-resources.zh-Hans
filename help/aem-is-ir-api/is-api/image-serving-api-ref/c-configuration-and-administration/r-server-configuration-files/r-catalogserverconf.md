---
description: 包含與管理影像目錄相關的設定。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

包含與管理影像目錄相關的設定。

此檔案是JAVA屬性檔案。 務必遵循適當的慣例；否則 [!DNL Platform Server] 可能無法啟動。 在Windows檔案路徑中使用雙反斜線&#39;\\&#39;或單正斜線&#39;/&#39;，而非反斜線&#39;\&#39;。 在此型別的檔案中，反斜線會作為逸出字元使用。

此檔案的變更會在檔案儲存後不久生效。

只有下列設定可以在中變更 [!DNL catalog-service.conf]. 如果特定設定不存在，則可以在檔案中的任意位置新增該設定。 每個設定只能有一個例項。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
