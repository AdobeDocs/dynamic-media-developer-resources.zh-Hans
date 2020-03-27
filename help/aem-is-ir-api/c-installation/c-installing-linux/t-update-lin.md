---
description: 在Linux上升级Scene7图像服务时，请按照此过程操作。
seo-description: 在Linux上升级Scene7图像服务时，请按照此过程操作。
seo-title: 从IS 4.7.4或更高版本进行更新
solution: Experience Manager
title: 从IS 4.7.4或更高版本进行更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 从IS 4.7.4或更高版本进行更新{#updating-from-is-or-later}

在Linux上升级Scene7图像服务时，请按照此过程操作。

如果您是从旧版本的图像服务升级，请联系支持部门以获得正确的过程。

升级 [!DNL webapps] 时可能会删除该文件夹。 请在升级之前 [!DNL webapps] 备份文件夹。

1. 以根权限登录到服务器主机。
1. 解压缩和解压缩图像服务分发tar文件。
1. 运 [!DNL ./install-is] 行以启动位于文件夹中的安装向 [!DNL setup] 导。

   更新安装程序会检查已安装包的完整性和版本。 如果成功，则显示最终用户许可协议(“EULA”)。
1. 阅读许可协议，然后输入“ **[!UICONTROL y]**”以继续安装。

   安装程序将旧的服务器配置文件备份到该文 [!DNL BACKUP/] 件夹。

   安装完成后，将显示以下消息：

   `Image Server was started successfully`
>在更新过程中，文 [!DNL ImageServing/conf/server.xml] 件会更新为最新设置。 如果您已更改或添加了任何值，则应保存现有值， [!DNL server.xml] 并在升级后重新实施更改。
>
>安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅实用程 [!DNL playlog] 序的说明。

