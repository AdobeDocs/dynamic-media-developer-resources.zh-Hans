---
title: 验证安装
description: 安装Dynamic Media映像服务后，应验证安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 验证安装 {#verifying-the-installation}

安装Dynamic Media映像服务后，应验证安装。

映像服务器安装为Windows服务。

1. 打开服务控制面板并检查 `Dynamic Media Image Serving` 存在，状态为 `Started`.
1. 在同一台主机或另一台主机上打开Internet浏览器，并检查默认服务器响应：

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

检查是否存在&quot; `imageServer.`”项，表示图像服务器正在侦听。
>可以使用文档和演示软件包的示例页面（如果已安装）执行其他验证。
