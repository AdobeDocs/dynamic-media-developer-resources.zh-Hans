---
description: 在Linux上安装映像服务后，请验证安装。
seo-description: 在Linux上安装映像服务后，请验证安装。
seo-title: 验证安装
solution: Experience Manager
title: 验证安装
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# 验证安装{#verifying-the-installation}

在Linux上安装映像服务后，请验证安装。

映像服务器作为Linux守护程序安装。

**验证安装**

1. 验证图像服务是否已配置为自动开始且是否正在运行：

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >您必须具有根权限才能运行这些脚本。

1. 打开同一主机或不同主机上的因特网浏览器并检查默认服务器响应：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

在响应中，检查是否存在以“ `imageServer.`”开头的项，这表示平台服务器可以成功与图像服务器通信。
>如果已安装，可使用文档和演示包的示例页执行其他验证。

