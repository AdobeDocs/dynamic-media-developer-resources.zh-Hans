---
title: 验证安装
description: 安装Dynamic Media图像服务后，应验证安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 验证安装 {#verifying-the-installation}

安装Dynamic Media图像服务后，应验证安装。

映像服务器安装为Windows服务。

1. 打开服务控制面板并检查`Dynamic Media Image Serving`是否存在，且状态为`Started`。
1. 在同一台主机或另一台主机上打开Internet浏览器，并检查默认服务器响应：

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

检查响应中是否存在“`imageServer.`”项，这表示图像服务器正在侦听。

>如果安装了，则可以使用文档和演示软件包的示例页面执行其他验证。
