---
description: 使用這些伺服器設定進行SSL。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SSL{#ssl}

使用這些伺服器設定進行SSL。

## TC：：SslPort — 接聽連線埠 {#section-c80eb582bf684b3fa7313a77cc606769}

指定監聽連線埠 [!DNL Platform Server] 用於SSL連線。 默认值为 8443。

## TC：：keystoreFile - Keystore檔案路徑 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL Keystore檔案的路徑/名稱。 可以是絕對路徑或相對於[！DNL]的路徑 *[!DNL install_folder]*/conf]。 預設為 *install_folder*/conf/scene7keystore。

## TC：：keystorePass — 金鑰庫密碼 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

keystore檔案的密碼。 默认值为 `scene7`.

## TC：：keystoreType - Keystore型別 {#section-8f263e1ba67740728cd39181960d7c7d}

選取金鑰庫的型別。 &#39; `Java'` （預設）和&#39; `PKCS12`支援&#39;。
