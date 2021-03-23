---
description: 在Linux上升级Dynamic Media图像服务时，请使用此过程。
seo-description: 在Linux上升级Dynamic Media图像服务时，请使用此过程。
seo-title: 从IS 4.7.4或更高版本进行更新
solution: Experience Manager
title: 从IS 4.7.4或更高版本进行更新
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 从IS 4.7.4或更高版本{#updating-from-is-or-later}进行更新

在Linux上升级Dynamic Media图像服务时，请使用此过程。

如果您是从旧版本的图像服务升级，请联系支持部门以获得正确的过程。

升级时可删除[!DNL webapps]文件夹。 请在升级前备份[!DNL webapps]文件夹。

1. 以根权限登录到服务器主机。
1. 解压缩并解压缩图像服务分发tar文件。
1. 运行[!DNL ./install-is]以启动位于[!DNL setup]文件夹中的安装向导。

   更新安装程序会检查已安装包的完整性和版本。 如果成功，则显示最终用户许可协议(“EULA”)。
1. 阅读许可协议，然后输入“ **[!UICONTROL y]**”以继续安装。

   安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`

在更新过程中，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果您已更改或添加了任何值，则应保存现有[!DNL server.xml]并在升级后重新实施您所做的更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅[!DNL playlog]实用程序的说明。
