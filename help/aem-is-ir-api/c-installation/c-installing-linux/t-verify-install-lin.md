---
title: 验证安装
description: 在Linux®上安装映像服务后，请验证是否已安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 验证安装{#verifying-the-installation}

在Linux®上安装映像服务后，请验证是否已安装。

Image Server作为Linux®守护程序安装。

**验证安装**

1. 验证图像服务是否已配置为自动启动并且正在运行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必须具有root权限才能运行这些脚本。

1. 在同一台主机或另一台主机上打开Internet浏览器，并检查默认服务器响应：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

在响应中，检查是否存在以`imageServer`开头的项，这表示[!DNL Platform Server]可以成功与图像服务器通信。

>如果安装了，则可以使用文档和演示软件包的示例页面执行其他验证。
