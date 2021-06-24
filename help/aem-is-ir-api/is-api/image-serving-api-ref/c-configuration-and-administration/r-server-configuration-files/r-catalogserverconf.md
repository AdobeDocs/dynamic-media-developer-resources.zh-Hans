---
description: 包含与管理图像目录相关的设置。
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

包含与管理图像目录相关的设置。

此文件是JAVA属性文件。 必须注意遵守适当的公约；否则，平台服务器可能无法启动。 在Windows文件路径中，使用双反斜杠“\\”或单正斜杠“/”，而不是反斜杠“\”。 在此类型的文件中，反斜线用作转义字符。

对此文件所做的更改在保存文件后不久生效。

[!DNL catalog-service.conf]中只能更改下面列出的设置。 如果缺少特定设置，则可以在文件中的任意位置添加该设置。 每个设置只能有一个实例。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
