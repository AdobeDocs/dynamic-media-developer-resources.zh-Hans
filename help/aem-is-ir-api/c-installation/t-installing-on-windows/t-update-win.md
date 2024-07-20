---
title: 从IS 4.7.4或更高版本更新
description: 升级Dynamic Media图像服务时，请使用此过程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 从IS 4.7.4或更高版本更新{#updating-from-is-or-later}

升级Dynamic Media图像服务时，请使用此过程。

如果您是从旧版本的图像服务升级，请联系支持人员来获取正确的流程。

>[!NOTE]
>
>升级时可能会删除[!DNL webapps]文件夹。 在升级之前备份[!DNL webapps]文件夹。

1. 使用管理权限登录到您的服务器主机。
1. 提取图像服务分发zip文件的内容。
1. 运行`setup/setup.exe`启动安装向导。
1. 选择&#x200B;**[!UICONTROL 下一步]**&#x200B;进入最终用户许可协议(EULA)，阅读许可协议，然后选择&#x200B;**[!UICONTROL 是]**。

   下一页显示以前的配置设置。
1. 单击&#x200B;**[!UICONTROL 下一步]**&#x200B;开始更新安装。

   >[!NOTE]
   >
   >安装程序将旧服务器配置文件备份到[!DNL BACKUP/]文件夹。

1. 安装完成后，选择&#x200B;**[!UICONTROL 完成]**&#x200B;退出安装向导。

   有时，安装向导可能会要求您重新启动系统。

在更新期间，[!DNL ImageServing/conf/server.xml]文件将更新为最新设置。 如果您更改或添加了任何值，则应保存现有[!DNL server.xml]，并在升级后重新实施更改。

进行更新安装后，请考虑先预热HTTP响应缓存，然后再使服务器处于活动状态。 有关详细信息，请参阅`playlog`实用程序的说明。
