---
title: 驗證安裝
description: 安裝Dynamic Media Image Serving後，請務必確認安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 驗證安裝 {#verifying-the-installation}

安裝Dynamic Media Image Serving後，請務必確認安裝。

影像伺服器會安裝為Windows服務。

1. 開啟「服務控制面板」並檢查 `Dynamic Media Image Serving` 以以下狀態存在 `Started`.
1. 開啟相同或不同主機上的網際網路瀏覽器，並檢查預設伺服器回應：

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

檢查是否存在&quot; `imageServer.`」個專案，表示影像伺服器正在接聽。
>若已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
