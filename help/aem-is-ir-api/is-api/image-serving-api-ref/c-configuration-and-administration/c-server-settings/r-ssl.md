---
description: 将这些服务器设置用于SSL。
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

将这些服务器设置用于SSL。

## TC：：SslPort — 侦听端口 {#section-c80eb582bf684b3fa7313a77cc606769}

指定监听端口 [!DNL Platform Server] 用于SSL连接。 默认值为 8443。

## TC：：keystoreFile - Keystore文件路径 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密钥库文件的路径/名称。 可以是绝对路径或相对于[！DNL的路径 *[!DNL install_folder]*/conf]。 默认为 *install_folder*/conf/scene7keystore.

## TC：：keystorePass - Keystore密码 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密钥库文件的密码。 默认值为 `scene7`.

## TC：：keystoreType — 密钥库类型 {#section-8f263e1ba67740728cd39181960d7c7d}

选择密钥库的类型。 ‘ `Java'` （默认）和&#39; `PKCS12`支持&#39;。
