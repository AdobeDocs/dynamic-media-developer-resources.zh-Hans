---
description: 将这些服务器设置用于SSL。
seo-description: 将这些服务器设置用于SSL。
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---


# SSL{#ssl}

将这些服务器设置用于SSL。

## TC::SslPort —— 侦听端口{#section-c80eb582bf684b3fa7313a77cc606769}

指定平台服务器的SSL连接监听端口。 默认值为 8443。

## TC::keystoreFile —— 密钥库文件路径{#section-0cdf9b3cfcf249818b22221d01bafebe}

指定SSL密钥库文件的路径／名称。 可以是相对于[!DNL *[!DNL install_folder]*/conf]的绝对路径或路径。 默认值为&#x200B;*install_folder*/conf/scene7keystore。

## TC::keystorePass —— 密钥库密码{#section-e7e9bfb7df584a248c0e3ee46803c3b1}

密钥库文件的口令。 默认值为 `scene7`.

## TC::keystoreType - Keystore类型{#section-8f263e1ba67740728cd39181960d7c7d}

选择密钥库的类型。 支持“ `Java'`（默认）和“ `PKCS12`”。
