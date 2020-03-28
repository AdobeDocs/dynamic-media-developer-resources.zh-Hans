---
description: 升级Scene7图像服务时，请按照此过程操作。
seo-description: 升级Scene7图像服务时，请按照此过程操作。
seo-title: 从IS 4.7.4或更高版本进行更新
solution: Experience Manager
title: 从IS 4.7.4或更高版本进行更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 从IS 4.7.4或更高版本进行更新{#updating-from-is-or-later}

升级Scene7图像服务时，请按照此过程操作。

如果您是从旧版本的图像服务升级，请联系支持部门以获得正确的过程。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>升级 [!DNL webapps] 时可能会删除该文件夹。 升级前备 [!DNL webapps] 份文件夹。

1. 使用管理权限登录到服务器主机。
1. 解压图像服务分发zip文件的内容。
1. 运行setup/setup.exe以启动安装向导。
1. 单 **[!UICONTROL 击]** “下一步”进入最终用户许可协议(EULA)，阅读许可协议，然后单击“ **[!UICONTROL 是”]**。

   下一页显示以前的配置设置。
1. 单击 **[!UICONTROL 下一步]** ，以开始更新安装。

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >安装程序将旧的服务器配置文件备份到该文 [!DNL BACKUP/] 件夹。

1. 安装完成后，单击“完成”退出安装向导。

   在某些情况下，安装向导可能会要求重新启动系统。
>在更新过程中，文 [!DNL ImageServing/conf/server.xml] 件会更新为最新设置。 如果您已更改或添加了任何值，则应保存现有值， [!DNL server.xml] 并在升级后重新实施更改。
>
>安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅实用程 `playlog` 序的说明。

