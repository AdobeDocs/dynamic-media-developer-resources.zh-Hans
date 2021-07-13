---
description: 此过程说明如何在Linux上首次安装图像服务。
solution: Experience Manager
title: 首次安装
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 首次安装{#installing-for-the-first-time}

此过程说明如何在Linux上首次安装图像服务。

1. 使用根权限登录到服务器主机。
1. 创建文件夹[!DNL /usr/local/scene7/licenses]。

   如果“图像提供”和/或“图像呈现”许可证密钥文件（带有[!DNL .sc8]文件后缀）可用，请将其复制到此文件夹。 否则，请继续安装，稍后再安装许可证密钥。
1. 解压缩和解压缩图像服务分发tar文件。
1. 运行位于[!DNL Setup]文件夹中的[!DNL ./install-is]以启动安装向导。

   如果未找到许可证密钥，则会显示说明如何获取许可证文件的说明。 此时执行此操作，或继续安装映像服务，稍后安装许可证密钥。
1. 显示最终用户许可协议(EULA)时，请阅读许可协议，然后输入`y`以继续。

   安装程序会显示下表中列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主监听端口[8080]:</span> </p> </td> 
   <td colname="col2"> <p>用于图像提供和图像渲染的主HTTP侦听端口。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理员监听端口[8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理员监听端口。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大HTTP缓存大小(MB)[2000]:</span> </p> </td> 
   <td colname="col2"> <p>主响应缓存的初始大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 缓存根文件夹[/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS缓存文件夹。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器所有者ID [根]:</span> </p> </td> 
   <td colname="col2"> <p>安装图像服务器的用户帐户。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器组ID [根]:</span> </p> </td> 
   <td colname="col2"> <p>安装图像服务器的组帐户。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 按&#x200B;**[!UICONTROL Enter]**&#x200B;接受默认值或指定其他值。

   确保指定的所有端口号都是唯一的，并且不会在此主机上使用。

   >[!IMPORTANT]
   >
   >如果指定了除根帐户之外的其他帐户，则必须确保在配置文件中重新配置图像服务器需要读取和/或写入的所有文件和文件夹时，这些文件夹的访问权限均正确设置。
   >
   >映像服务现已安装到[!DNL /usr/local/Scene7/ImageServing]。 某些图像渲染内容已安装到[!DNL /usr/local/Scene7/ImageRendering]中。
   >
   >在安装结束时，安装向导会尝试启动Image Server。 如果未找到有效的许可证密钥，则无法启动图像服务器。 如果存在有效的许可证，并且图像服务器仍未启动，请查阅日志文件。

>[!NOTE]
>
>如果安装映像服务后安装了许可证，则必须先手动启动映像服务器，然后才能使用。
