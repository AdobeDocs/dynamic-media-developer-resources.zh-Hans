---
title: 从IS 4.7.4或更高版本进行更新
description: 升级Dynamic Media图像服务时，请使用此过程。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 从IS 4.7.4或更高版本进行更新{#updating-from-is-or-later}

升级Dynamic Media图像服务时，请使用此过程。

如果您从旧版图像服务升级，请联系支持人员以获取正确的过程。

>[!NOTE]
>
>的 [!DNL webapps] 升级时可删除文件夹。 备份 [!DNL webapps] 文件夹。

1. 使用管理权限登录服务器主机。
1. 提取图像服务分发zip文件的内容。
1. 通过运行 `setup/setup.exe`.
1. 选择 **[!UICONTROL 下一个]** 要前进到最终用户许可协议(EULA)，请阅读许可协议，然后选择 **[!UICONTROL 是]**.

   下一页显示之前的配置设置。
1. 单击 **[!UICONTROL 下一个]** 以启动更新安装。

   >[!NOTE]
   >
   >安装程序将旧的服务器配置文件备份到 [!DNL BACKUP/] 文件夹。

1. 安装完成后，选择 **[!UICONTROL 完成]** 退出安装向导。

   有时，安装向导可能会要求您重新启动系统。

在更新期间， [!DNL ImageServing/conf/server.xml] 文件将更新为最新设置。 如果您更改或添加了任何值，则应保存现有的 [!DNL server.xml] 和会在升级后重新实施您所做的更改。

安装更新后，请考虑在使服务器处于活动状态之前预热HTTP响应缓存。 请参阅 `playlog` 实用程序。
