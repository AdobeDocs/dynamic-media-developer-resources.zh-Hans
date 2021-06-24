---
description: 在Linux上升级Dynamic Media Image Serving时，请使用此过程。
solution: Experience Manager
title: 从IS 4.7.4或更高版本进行更新
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 从IS 4.7.4或更高版本进行更新{#updating-from-is-or-later}

在Linux上升级Dynamic Media Image Serving时，请使用此过程。

如果您从旧版图像服务升级，请联系支持人员以获取正确的过程。

升级时可以删除[!DNL webapps]文件夹。 请在升级前备份[!DNL webapps]文件夹。

1. 使用根权限登录到服务器主机。
1. 解压缩和解压缩图像服务分发tar文件。
1. 运行[!DNL ./install-is]以启动安装向导，该向导位于[!DNL setup]文件夹中。

   更新安装程序会检查已安装包的完整性和版本。 如果成功，则会显示最终用户许可协议(“EULA”)。
1. 阅读许可协议，然后输入“ **[!UICONTROL y]**”以继续安装。

   安装程序将旧的服务器配置文件备份到[!DNL BACKUP/]文件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`

在更新期间，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果已更改或添加任何值，则应保存现有的[!DNL server.xml]，并在升级后重新实施更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅[!DNL playlog]实用程序的说明。
