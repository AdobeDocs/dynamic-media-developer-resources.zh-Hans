---
description: 将这些服务器设置用于SSL。
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
TQID: 'https://experienceleague.adobe.com/VOdDIzV6b9J9AZ-qZyAj3AI77MukT1BbSzM-UM-B5N4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 2%

---

# SSL{#ssl}

将这些服务器设置用于SSL。

## TC：：SslPort — 侦听端口 {#section-c80eb582bf684b3fa7313a77cc606769}

为SSL连接指定[!DNL Platform Server]的侦听端口。 默认值为8443。

## TC：：keystoreFile - Keystore文件路径 {#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密钥库文件的路径/名称。 可以是绝对路径或相对于[!DNL *[!DNL install_folder]*/conf]的路径。 默认值为&#x200B;*install_folder*/conf/scene7keystore。

## TC：：keystorePass - Keystore密码 {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密钥库文件的密码。 默认值为`scene7`。

## TC：：keystoreType — 密钥库类型 {#section-8f263e1ba67740728cd39181960d7c7d}

选择密钥库的类型。 支持“`Java'`”（默认）和“`PKCS12`”。
