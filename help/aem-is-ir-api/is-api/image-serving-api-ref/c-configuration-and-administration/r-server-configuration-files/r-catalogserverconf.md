---
description: 包含与管理图像目录相关的设置。
seo-description: 包含与管理图像目录相关的设置。
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# catalog-server.conf{#catalog-server-conf}

包含与管理图像目录相关的设置。

此文件是JAVA属性文件。 必须注意遵守适当的公约；否则平台服务器可能无法开始。 在Windows文件路径中，使用多次反斜杠“\\”或单个正斜杠“/”而不是反斜杠“\”。 反斜杠用作此类型文件中的转义字符。

对此文件所做的更改在保存文件后不久生效。

仅可在中更改以下列出的设置 [!DNL catalog-service.conf]。 如果某个特定设置不存在，则可以在文件的任意位置添加该设置。 每个设置只能有一个实例。

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
