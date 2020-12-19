---
description: 在Linux上升级Scene7图像服务时，请使用此过程。
seo-description: 在Linux上升级Scene7图像服务时，请使用此过程。
seo-title: 从IS 4.7.4或更高版本更新
solution: Experience Manager
title: 从IS 4.7.4或更高版本更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# 从IS 4.7.4或更高版本{#updating-from-is-or-later}进行更新

在Linux上升级Scene7图像服务时，请使用此过程。

如果您是从旧版图像服务升级，请联系支持人员以获得正确的流程。

升级时可删除[!DNL webapps]文件夹。 请在升级前备份[!DNL webapps]文件夹。

1. 以根权限登录到服务器主机。
1. 解压缩和解压图像服务分发tar文件。
1. 运行[!DNL ./install-is]以启动位于[!DNL setup]文件夹中的安装向导。

   更新安装程序检查已安装包的完整性和版本。 如果成功，则显示最终用户许可协议(“EULA”)。
1. 阅读许可协议，然后输入“**[!UICONTROL y]**”以继续安装。

   安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`

在更新过程中，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果已更改或添加任何值，则应保存现有[!DNL server.xml]并在升级后重新实施更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅[!DNL playlog]实用程序的说明。
