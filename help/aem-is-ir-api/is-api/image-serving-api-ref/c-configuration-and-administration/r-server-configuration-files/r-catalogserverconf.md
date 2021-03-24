---
description: 包含与管理图像目录相关的设置。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

包含与管理图像目录相关的设置。

此文件是JAVA属性文件。 必须注意遵守适当的公约；否则平台服务器可能无法开始。 在Windows文件路径中，使用多次反斜杠“\\”或单个正斜杠“/”，而不是反斜杠“\”。 反斜杠用作此类型文件中的转义字符。

对此文件所做的更改在保存文件后不久生效。

[!DNL catalog-service.conf]中只能更改以下列出的设置。 如果某个特定设置不存在，则可在文件的任意位置添加该设置。 每个设置只能有一个实例。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
