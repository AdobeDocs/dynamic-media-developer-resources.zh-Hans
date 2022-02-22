---
title: 验证安装
description: 安装Dynamic Media Image Serving后，应验证安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 验证安装 {#verifying-the-installation}

安装Dynamic Media Image Serving后，应验证安装。

图像服务器作为Windows服务安装。

1. 打开“服务”控制面板并检查 `Dynamic Media Image Serving` 状态为 `Started`.
1. 在同一或其他主机上打开Internet浏览器，并检查默认服务器响应：

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

检查是否存在“ `imageServer.`“ ”项，表示图像服务器正在侦听。
>如果已安装，可以使用文档和演示包的示例页面执行其他验证。
