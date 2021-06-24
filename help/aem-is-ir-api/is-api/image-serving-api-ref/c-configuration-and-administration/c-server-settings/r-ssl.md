---
description: 将这些服务器设置用于SSL。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# SSL{#ssl}

将这些服务器设置用于SSL。

## TC::SslPort — 侦听端口 {#section-c80eb582bf684b3fa7313a77cc606769}

为SSL连接指定平台服务器的侦听端口。 默认值为 8443。

## TC::keystoreFile - Keystore文件路径 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密钥库文件的路径/名称。 可以是相对于[!DNL *[!DNL install_folder]*/conf]的绝对路径或路径。 默认值为&#x200B;*install_folder*/conf/scene7keystore。

## TC::keystorePass - Keystore密码 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密钥库文件的密码。 默认值为 `scene7`.

## TC::keystoreType - Keystore类型 {#section-8f263e1ba67740728cd39181960d7c7d}

选择密钥库的类型。 支持“ `Java'`（默认）和“ `PKCS12`”。
