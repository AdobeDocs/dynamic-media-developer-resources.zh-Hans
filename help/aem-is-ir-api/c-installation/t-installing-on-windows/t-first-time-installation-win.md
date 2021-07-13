---
description: 使用这些步骤在Windows上首次安装图像服务。
solution: Experience Manager
title: 首次安装
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 首次安装{#installing-for-the-first-time}

使用这些步骤在Windows上首次安装图像服务。

1. 使用管理权限登录服务器主机。
1. 如果您已经收到许可证，请将其复制到服务器，然后双击文件以运行许可证安装。

   如果您还没有许可证，则可以继续安装，稍后再安装许可证。
1. 提取图像服务分发zip文件的内容。
1. 运行[!DNL setup]/ [!DNL setup.exe]以启动安装向导。
1. 单击“下一步”前进到最终用户许可协议(EULA)，阅读许可协议，然后单击&#x200B;**[!UICONTROL 是]**。

   下面将显示[!DNL Authentication]对话框。
1. 如果已安装许可证，并且许可证信息显示在[!DNL Authentication]对话框中，请单击&#x200B;**[!UICONTROL Next]**&#x200B;以继续。

   如果您没有许可证，请单击&#x200B;**[!UICONTROL 请求许可证]**。 下一个对话框显示您计算机的网络接口卡MAC地址之一。 按提示的指示，向此MAC地址、您的公司名称和您正在安装的产品发送电子邮件。

   **重要信息：** 许可证基于此主机上安装的其中一个网络接口卡的MAC地址。如果禁用、删除或替换此卡，则许可证将不再被识别为有效。 确保获得将用于IS的硬件配置的许可证。

   如果没有有效的许可证，您可以继续安装IS，稍后再安装该许可证。 要继续，请单击&#x200B;**[!UICONTROL 返回]**&#x200B;以返回到[!DNL Authentication]对话框，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 转到“Platform Server管理设置”页面。 根据需要输入新值或接受默认值。

   您可以配置以下项目：

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> 平台服务器HTTP连接端口 </p> </td> 
   <td> <p>用于图像提供和图像渲染的主HTTP侦听端口 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 管理员监听端口 </p> </td> 
   <td> <p>管理员监听端口 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台服务器缓存大小(MB) </p> </td> 
   <td> <p>主响应缓存的初始大小 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 平台服务器缓存位置 </p> </td> 
   <td> <p>PS缓存文件夹 </p> </td> 
  </tr> 
 </tbody> 
</table>

指定的端口号必须唯一，不能由其他应用程序或服务使用。

下一个屏幕提供了查看所选设置的机会。
1. 单击&#x200B;**[!UICONTROL 返回]**&#x200B;进行更改，或单击&#x200B;**[!UICONTROL 下一步]**&#x200B;开始安装。
1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;退出安装向导。
