---
description: 安装Dynamic Media Image Serving后，应验证安装。
solution: Experience Manager
title: 验证安装
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# 验证安装{#verifying-the-installation}

安装Dynamic Media Image Serving后，应验证安装。

图像服务器作为Windows服务安装。

1. 打开“服务”控制面板并检查“Dynamic Media图像服务”是否处于“已开始”状态。
1. 打开同一或不同主机上的Internet浏览器并检查默认服务器响应：

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

检查响应中是否存在“ `imageServer.`”项，这表示图像服务器正在侦听。
>如果已安装，可使用文档和演示包的示例页执行其他验证。

