---
description: 此 [!DNL Platform Server] 除非要求標示為不可快取，否則會將所有回覆影像和特定文字資料快取到磁碟。
solution: Experience Manager
title: 回應資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 回應資料快取{#response-data-cache}

此 [!DNL Platform Server] 除非要求標示為不可快取，否則會將所有回覆影像和特定文字資料快取到磁碟。

的位置 [!DNL Platform Server]的磁碟快取設定為 `PS::cache.rootPaths`.

對於快取命中率高的應用程式，您可以在多個磁碟裝置之間分配回應資料快取，以提高伺服器效能和容量。 您可在每個磁碟上建立快取根資料夾，並在中註冊這些資料夾，即可完成此作業 `PS::cache.rootPaths`.

`PS::cache.maxSize` 指定所有快取專案的總大小，不考慮任何檔案系統負荷。 實際需要的磁碟空間量取決於檔案系統屬性（例如磁碟區塊大小）和快取專案數量。 建議為HTTP磁碟快取保留兩倍的磁碟空間，其數量由以下指定 `PS::cache.maxSize`. 系統會使用最近最少使用的演演算法，將快取資料量保持在限制內。

除了 `PS::cache.maxSize`，回應快取也是透過限制快取專案的最大數量來管理 `PS::cache.maxEntries`. 在Linux上，此設定所指定的值不得大於快取分割上可用的inode數目。

>[!NOTE]
>
>此 [!DNL Platform Server] 維護記憶體中的快取索引。 此索引的大小是32個位元組乘以 `PS::cache.maxEntries`. 您可能需要增加 [!DNL Platform Server] 棧集大小以容納較大的快取。

當伺服器依序關閉時，系統會使用儲存至磁碟的快取索引檔案。 萬一發生意外事件（例如電源故障），可能無法儲存此檔案。 此外，可能需要幾分鐘的時間才能完成 [!DNL Platform Server] 準備就緒。
