---
description: 在Linux上安装映像服务后，请验证安装。
solution: Experience Manager
title: 验证安装
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '137'
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

1. 打开同一或不同主机上的Internet浏览器并检查默认服务器响应：

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

在响应中，检查是否存在以“`imageServer.`”开头的项，这表示平台服务器可以成功与图像服务器通信。
>如果已安装，可使用文档和演示包的示例页执行其他验证。

