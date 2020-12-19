---
description: 升级Scene7图像服务时，请使用此过程。
seo-description: 升级Scene7图像服务时，请使用此过程。
seo-title: 从IS 4.7.4或更高版本更新
solution: Experience Manager
title: 从IS 4.7.4或更高版本更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# 从IS 4.7.4或更高版本{#updating-from-is-or-later}进行更新

升级Scene7图像服务时，请使用此过程。

如果您是从旧版图像服务升级，请联系支持人员以获得正确的流程。

>[!NOTE]
>
>升级时可删除[!DNL webapps]文件夹。 升级前备份[!DNL webapps]文件夹。

1. 以管理权限登录到服务器主机。
1. 提取图像服务分发zip文件的内容。
1. 运行setup/setup.exe以启动安装向导。
1. 单击&#x200B;**[!UICONTROL Next]**&#x200B;进入最终用户许可协议(EULA)，阅读许可协议，然后单击&#x200B;**[!UICONTROL 是]**。

   下一页显示以前的配置设置。
1. 单击&#x200B;**[!UICONTROL Next]**&#x200B;开始更新安装。

   >[!NOTE]
   >
   >安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

1. 安装完成后，单击“完成”退出安装向导。

   在某些情况下，安装向导可能会要求重新启动系统。

在更新过程中，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果已更改或添加任何值，则应保存现有[!DNL server.xml]并在升级后重新实施更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅`playlog`实用程序的说明。
