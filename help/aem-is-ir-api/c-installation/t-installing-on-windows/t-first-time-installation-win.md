---
title: 首次安装
description: 使用这些步骤在Windows上首次安装映像服务。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 首次安装{#installing-for-the-first-time}

使用这些步骤在Windows上首次安装映像服务。

1. 使用管理权限登录到您的服务器主机。
1. 如果您已经收到许可证，请将其复制到服务器，然后双击该文件运行许可证安装。

   如果您还没有许可证，可以继续安装并在以后安装许可证。

1. 提取图像服务分发zip文件的内容。
1. 通过运行[!DNL setup]/ [!DNL setup.exe]启动安装向导。
1. 选择&#x200B;**[!UICONTROL 下一步]**&#x200B;进入最终用户许可协议(EULA)，阅读许可协议，然后选择&#x200B;**[!UICONTROL 是]**。

   随后将显示[!DNL Authentication]对话框。
1. 如果已安装许可证，并且许可证信息显示在[!DNL Authentication]对话框中，请选择&#x200B;**[!UICONTROL 下一步]**&#x200B;以继续。

   如果您没有许可证，请选择&#x200B;**[!UICONTROL 请求许可证]**。 下一个对话框显示计算机的一个网络接口卡MAC地址。 根据提示指示，通过电子邮件发送此MAC地址、公司名称和要安装的产品。

   **重要信息：**&#x200B;许可证基于此主机上安装的某个网卡的MAC地址。 如果禁用、移除或替换此卡，则许可证不再被识别为有效。 请确保获得用于图像服务的硬件配置的许可证。

   如果没有有效的许可证，您可以继续安装IS，稍后再安装许可证。 若要继续，请选择&#x200B;**[!UICONTROL 上一步]**&#x200B;以返回[!DNL Authentication]对话框，然后选择&#x200B;**[!UICONTROL 下一步]**。
1. 继续访问“[!DNL Platform Server]管理员设置”页面。 根据需要输入新值或接受默认值。

   您可以配置以下项目：

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP连接端口 </p> </td>
      <td> <p>用于图像服务和图像渲染的主HTTP侦听端口 </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理员侦听端口 </p> </td>
      <td> <p>管理员侦听端口 </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server]缓存大小(MB) </p> </td>
      <td> <p>主响应缓存的初始大小 </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server]缓存位置 </p> </td>
      <td> <p>PS缓存文件夹 </p> </td>
   </tr>
   </tbody>
   </table>

   指定的端口号必须是唯一的，并且不能由其他应用程序或服务使用。

   下一个屏幕提供了查看所选设置的机会。

1. 选择&#x200B;**[!UICONTROL 上一步]**&#x200B;以进行更改，或选择&#x200B;**[!UICONTROL 下一步]**&#x200B;开始安装。

1. 选择&#x200B;**[!UICONTROL 完成]**&#x200B;以退出安装向导。
