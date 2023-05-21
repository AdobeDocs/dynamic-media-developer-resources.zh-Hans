---
title: 驗證安裝
description: 在Linux®上安裝「影像伺服」後，請確認是否已安裝。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 驗證安裝{#verifying-the-installation}

在Linux®上安裝「影像伺服」後，請確認是否已安裝。

Image Server會安裝為Linux®精靈。

**驗證安裝的方式**

1. 確認「影像伺服」已設定為自動啟動，且執行中：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必須具有root許可權才能執行這些指令碼。

1. 開啟相同或不同主機上的網際網路瀏覽器，並檢查預設伺服器回應：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

在回應中，檢查開頭為的專案是否存在 `imageServer`，表示 [!DNL Platform Server] 可成功與影像伺服器通訊。

>若已安裝，可使用檔案和示範套件的範例頁面執行其他驗證。
