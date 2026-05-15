---
title: 从IS 4.7.4或更高版本更新
description: 在Linux®上升级Dynamic Media图像服务时，请使用此过程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
TQID: 'https://experienceleague.adobe.com/RGRlIuemg6bPstlymZg7Ajr9i2ANq-HNjoIULaJydfs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 0%

---

# 从IS 4.7.4或更高版本更新{#updating-from-is-or-later}

在Linux®上升级Dynamic Media图像服务时，请使用此过程。

如果您是从旧版本的图像服务升级，请联系支持人员来获取正确的流程。

升级时可以删除[!DNL webapps]文件夹。 请在升级前备份[!DNL webapps]文件夹。

1. 使用root权限登录到您的服务器主机。
1. 解压缩并解压缩图像服务分发tar文件。
1. 在[!DNL setup]文件夹中，运行[!DNL `./install-is`]以启动安装向导。

   更新安装程序会检查已安装软件包的完整性和版本。 如果成功，将显示“最终用户许可协议”(“EULA”)。
1. 阅读许可协议，然后输入&#x200B;**[!UICONTROL y]**&#x200B;以继续安装。

   安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`

在更新期间，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果您更改或添加了任何值，请保存现有[!DNL server.xml]，并在升级后重新实施更改。

进行更新安装后，请考虑先预热HTTP响应缓存，然后再使服务器处于活动状态。 有关详细信息，请参阅[!DNL playlog]实用程序的说明。
