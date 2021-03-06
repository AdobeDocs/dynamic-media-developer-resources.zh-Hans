---
title: 验证安装
description: 在Linux®上安装映像服务后，请验证安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# 验证安装{#verifying-the-installation}

在Linux®上安装映像服务后，请验证安装。

映像服务器作为Linux®守护程序安装。

**验证安装**

1. 验证“图像服务”是否配置为自动启动并且它正在运行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必须具有根权限才能运行这些脚本。

1. 在同一或其他主机上打开Internet浏览器，并检查默认服务器响应：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

在响应中，检查是否存在以 `imageServer`，表示平台服务器可以成功与图像服务器通信。

>如果已安装，可以使用文档和演示包的示例页面执行其他验证。
