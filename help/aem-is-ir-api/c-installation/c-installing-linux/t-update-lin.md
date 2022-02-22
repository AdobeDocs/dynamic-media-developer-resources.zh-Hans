---
title: 从IS 4.7.4或更高版本进行更新
description: 在Linux®上升级Dynamic Media Image Serving时，请使用此过程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 从IS 4.7.4或更高版本进行更新{#updating-from-is-or-later}

在Linux®上升级Dynamic Media Image Serving时，请使用此过程。

如果您从旧版图像服务升级，请联系支持人员以获取正确的过程。

的 [!DNL webapps] 升级时可以删除文件夹。 请备份 [!DNL webapps] 文件夹。

1. 使用根权限登录到服务器主机。
1. 解压缩和解压缩图像服务分发tar文件。
1. 在 [!DNL setup] 文件夹，运行 [!DNL `./install-is`] 启动安装向导。

   更新安装程序会检查已安装包的完整性和版本。 如果成功，则会显示最终用户许可协议(“EULA”)。
1. 阅读许可协议，然后输入 **[!UICONTROL y]** 以继续安装。

   安装程序将旧的服务器配置文件备份到 [!DNL BACKUP/] 文件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`

在更新期间， [!DNL ImageServing/conf/server.xml] 文件将更新为最新设置。 如果您更改或添加了任何值，请保存您现有的 [!DNL server.xml] 和会在升级后重新实施您所做的更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 请参阅 [!DNL playlog] 实用程序。
