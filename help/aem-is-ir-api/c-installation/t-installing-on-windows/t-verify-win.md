---
title: 验证安装
description: 安装Dynamic Media图像服务后，应验证安装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 104
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

