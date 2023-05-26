---
title: 首次安装
description: 使用这些步骤首次在Windows上安装映像服务。
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

使用这些步骤首次在Windows上安装映像服务。

1. 使用管理权限登录到您的服务器主机。
1. 如果已收到许可证，请将其复制到服务器，然后双击该文件运行许可证安装。

   如果您还没有许可证，可以继续安装并在以后安装许可证。

1. 提取图像服务分发zip文件的内容。
1. 通过运行启动安装向导 [!DNL setup]/ [!DNL setup.exe].
1. 选择 **[!UICONTROL 下一个]** 要前进到最终用户许可协议(EULA)，请阅读许可协议，然后选择 **[!UICONTROL 是]**.

   此 [!DNL Authentication] 对话框随即显示。
1. 如果已安装许可证，许可证信息会显示在 [!DNL Authentication] 对话框中，选择 **[!UICONTROL 下一个]** 以继续。

   如果您没有许可证，请选择 **[!UICONTROL 请求许可证]**. 下一个对话框显示计算机的一个网络接口卡MAC地址。 按照提示指示，通过电子邮件发送此MAC地址、公司名称和要安装的产品。

   **重要提示：** 许可证基于此主机上安装的其中一个网络接口卡的MAC地址。 如果禁用、移除或替换此卡，则许可证不再被识别为有效。 确保获得用于图像服务的硬件配置的许可证。

   在没有有效许可证的情况下，您可以继续安装IS，稍后再安装许可证。 要继续，请选择 **[!UICONTROL 返回]** 以返回 [!DNL Authentication] 对话框，然后选择 **[!UICONTROL 下一个]**.
1. 继续访问“[!DNL Platform Server] “管理员设置”页面。 根据需要输入新值或接受默认值。

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
      <td> <p> [!DNL Platform Server] 缓存大小（以MB为单位） </p> </td>
      <td> <p>主响应缓存的初始大小 </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] 缓存位置 </p> </td>
      <td> <p>PS缓存文件夹 </p> </td>
   </tr>
   </tbody>
   </table>

   指定的端口号必须是唯一的，并且不能由其他应用程序或服务使用。

   下一个屏幕提供了查看所选设置的机会。

1. 选择 **[!UICONTROL 返回]** 进行更改，或选择 **[!UICONTROL 下一个]** 以开始安装。

1. 选择 **[!UICONTROL 完成]** 以退出安装向导。
