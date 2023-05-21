---
description: 您可以在巢狀/內嵌請求中指定cache=on ，快取巢狀/內嵌影像伺服和影像演算請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。
solution: Experience Manager
title: 輔助資料快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 輔助資料快取{#auxiliary-data-caches}

您可以在巢狀/內嵌請求中指定cache=on ，快取巢狀/內嵌影像伺服和影像演算請求產生的中間影像資料。 此資料會以專屬格式儲存在回應資料快取中。

從外部HTTP伺服器取得的影像也會儲存在回應資料快取中。 產生快取專案之前，會先使用驗證公用程式自動驗證這類影像。

此 [!DNL Platform Server] 編譯影像目錄資料以有效存取。 此資料儲存在 `CS::CatalogCacheFolder`.
