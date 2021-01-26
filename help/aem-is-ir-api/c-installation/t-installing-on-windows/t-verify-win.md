---
description: 安装Dynamic Media图像服务后，应验证安装。
seo-description: 安装Dynamic Media图像服务后，应验证安装。
seo-title: 验证安装
solution: Experience Manager
title: 验证安装
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 验证安装{#verifying-the-installation}

安装Dynamic Media图像服务后，应验证安装。

图像服务器作为Windows服务安装。

1. 打开“服务”控制面板并检查“Dynamic Media图像服务”是否处于“已开始”状态。
1. 打开同一主机或不同主机上的因特网浏览器并检查默认服务器响应：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

检查响应中是否存在“ `imageServer.`”项，这表示图像服务器正在监听。
>如果已安装，可使用文档和演示包的示例页执行其他验证。

