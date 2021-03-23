---
description: 使用以下步骤在Windows上首次安装图像服务。
seo-description: 使用以下步骤在Windows上首次安装图像服务。
seo-title: 首次安装
solution: Experience Manager
title: 首次安装
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 首次安装{#installing-for-the-first-time}

使用以下步骤在Windows上首次安装图像服务。

1. 使用管理权限登录到服务器主机。
1. 如果您已收到许可证，请将其复制到服务器，然后通过多次单击文件来运行许可证安装。

   如果您还没有许可证，可以继续安装，稍后再安装许可证。
1. 解压图像服务分发zip文件的内容。
1. 运行[!DNL setup]/ [!DNL setup.exe]以启动安装向导。
1. 单击“下一步”前进到最终用户许可协议(EULA)，阅读许可协议，然后单击&#x200B;**[!UICONTROL 是]**。

   随后将显示[!DNL Authentication]对话框。
1. 如果已安装许可证，且许可证信息显示在[!DNL Authentication]对话框中，请单击&#x200B;**[!UICONTROL 下一步]**&#x200B;继续。

   如果您没有许可证，请单击&#x200B;**[!UICONTROL 请求许可证]**。 下一个对话框显示您计算机的网卡MAC地址之一。 按提示的指示，通过电子邮件发送此MAC地址、公司名称和您正在安装的产品。

   **重要：** 许可证基于安装在此主机上的某个网络接口卡的MAC地址。如果禁用、删除或更换此卡，则许可证将不再被识别为有效。 请务必获取将用于IS的硬件配置的许可证。

   如果没有有效的许可证，您可以继续安装IS，稍后再安装该许可证。 要继续，请单击&#x200B;**[!UICONTROL 返回]**&#x200B;返回到[!DNL Authentication]对话框，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 进入“平台服务器管理设置”页面。 根据需要输入新值或接受默认值。

   您可以配置以下项目：

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> 平台服务器HTTP连接端口 </p> </td> 
   <td> <p>用于图像服务和图像渲染的主HTTP侦听端口 </p> </td> 
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

指定的端口号必须是唯一的，不能由其他应用程序或服务使用。

下一个屏幕提供了查看选定设置的机会。
1. 单击&#x200B;**[!UICONTROL 返回]**&#x200B;进行更改，或单击&#x200B;**[!UICONTROL 下一步]**&#x200B;开始安装。
1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;退出安装向导。
