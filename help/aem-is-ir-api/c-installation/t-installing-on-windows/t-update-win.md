---
description: 升级Dynamic Media图像服务时，请使用此过程。
solution: Experience Manager
title: 从IS 4.7.4或更高版本进行更新
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# 从IS 4.7.4或更高版本{#updating-from-is-or-later}进行更新

升级Dynamic Media图像服务时，请使用此过程。

如果您是从旧版本的图像服务升级，请联系支持部门以获得正确的过程。

>[!NOTE]
>
>升级时可删除[!DNL webapps]文件夹。 升级前备份[!DNL webapps]文件夹。

1. 使用管理权限登录到服务器主机。
1. 解压图像服务分发zip文件的内容。
1. 运行setup/setup.exe以启动安装向导。
1. 单击&#x200B;**[!UICONTROL 下一步]**&#x200B;前进到最终用户许可协议(EULA)，阅读许可协议，然后单击&#x200B;**[!UICONTROL 是]**。

   下一页显示以前的配置设置。
1. 单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以开始更新安装。

   >[!NOTE]
   >
   >安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

1. 安装完成后，单击“完成”退出安装向导。

   在某些情况下，安装向导可能会要求重新启动系统。

在更新过程中，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果您已更改或添加了任何值，则应保存现有[!DNL server.xml]并在升级后重新实施您所做的更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 有关详细信息，请参阅`playlog`实用程序的说明。
