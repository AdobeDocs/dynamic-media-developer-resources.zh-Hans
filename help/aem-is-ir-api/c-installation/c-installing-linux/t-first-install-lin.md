---
title: 首次安装
description: 此过程说明如何在Linux®上首次安装映像服务。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 首次安装{#installing-for-the-first-time}

此过程说明如何在Linux®上首次安装映像服务。

1. 使用root权限登录到您的服务器主机。
1. 创建文件夹 [!DNL /usr/local/scene7/licenses].

   如果图像服务和/或图像渲染许可证密钥文件(包含 [!DNL .sc8] 文件后缀)，请将其复制到此文件夹。 否则，请继续安装并在以后安装许可证密钥。
1. 解压缩并解压缩图像服务分发tar文件。
1. 在 [!DNL Setup] 文件夹，通过运行安装向导来启动 [!DNL ./install-is].

   如果没有找到许可证密钥，则显示描述如何获取许可证文件的说明。 此时执行此操作，或者继续安装映像服务并稍后安装许可证密钥。
1. 显示最终用户许可协议(EULA)时，请阅读许可协议，然后输入 `y` 以继续。

   安装程序将显示下表中所列的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主侦听端口[8080]：</span> </p> </td>
   <td colname="col2"> <p>用于图像服务和图像渲染的主HTTP侦听端口。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理员侦听端口[8083]：</span> </p> </td> 
   <td colname="col2"> <p>管理员侦听端口。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大HTTP缓存大小(MB) [2000]：</span> </p> </td> 
   <td colname="col2"> <p>主响应缓存的初始大小。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 缓存根文件夹[/usr/local/scene7/ImageServing/cache]：</span> </p> </td> 
   <td colname="col2"> <p>ps缓存文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器所有者ID [root]：</span> </p> </td>
   <td colname="col2"> <p>要安装图像服务服务器的用户帐户。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器组ID [root]：</span> </p> </td>
   <td colname="col2"> <p>要安装图像服务服务器的组帐户。 </p> </td>
  </tr>
 </tbody>
</table>

1. 按 **[!UICONTROL 输入]** 接受默认值或指定其他值。

   请确保指定的所有端口号都是唯一的，否则不会在此主机上使用。

   >[!IMPORTANT]
   >
   >如果指定了root以外的帐户，则必须确保在配置文件中重新配置图像服务器需要读取和写入的所有文件和文件夹时，正确设置这些文件夹的访问权限。
   >
   >图像服务现已安装到 [!DNL /usr/local/Scene7/ImageServing]. 某些图像渲染内容安装到 [!DNL /usr/local/Scene7/ImageRendering].
   >
   >安装结束时，安装向导将尝试启动映像服务器。 如果未找到有效的许可证密钥，则图像服务器无法启动。 如果许可证有效，但图像服务器仍未启动，请查阅日志文件。

>[!NOTE]
>
>如果在安装映像服务后安装了许可证，则必须先手动启动映像服务器，然后才能使用。
