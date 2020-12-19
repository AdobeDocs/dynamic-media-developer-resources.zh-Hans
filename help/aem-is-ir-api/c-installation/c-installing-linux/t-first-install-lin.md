---
description: 此过程说明如何在Linux上首次安装图像服务。
seo-description: 此过程说明如何在Linux上首次安装图像服务。
seo-title: 首次安装
solution: Experience Manager
title: 首次安装
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# 首次安装{#installing-for-the-first-time}

此过程说明如何在Linux上首次安装图像服务。

1. 使用根权限登录到服务器主机。
1. 创建文件夹[!DNL /usr/local/scene7/licenses]。

   如果图像服务和／或图像渲染许可证密钥文件（带有[!DNL .sc8]文件后缀）可用，请将其复制到此文件夹。 否则，请继续安装，稍后再安装许可证密钥。
1. 解压缩和解压图像服务分发tar文件。
1. 运行[!DNL Setup]文件夹中的[!DNL ./install-is]以启动安装向导。

   如果未找到许可证密钥，则显示说明如何获取许可证文件。 此时执行此操作，或继续安装图像服务并稍后安装许可证密钥。
1. 显示最终用户许可协议(EULA)时，请阅读许可协议，然后输入`y`以继续。

   安装程序将显示下表中列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主监听端口[8080]:</span> </p> </td> 
   <td colname="col2"> <p>用于图像服务和图像渲染的主HTTP侦听端口。 </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"> 图像服务器所有者ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>要安装图像服务服务器的用户帐户。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器组ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>要安装图像服务服务器的组帐户。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 按&#x200B;**[!UICONTROL 输入]**&#x200B;接受默认值或指定其他值。

   确保指定的所有端口号都是唯一的，不要在此主机上使用。

   >[!IMPORTANT]
   >
   >如果指定了除根帐户以外的帐户，则必须确保在配置文件中重新配置这些文件夹时正确设置图像服务器需要读取和／或写入的所有文件和文件夹的访问权限。
   >
   >映像服务现已安装到[!DNL /usr/local/Scene7/ImageServing]。 某些图像渲染内容已安装到[!DNL /usr/local/Scene7/ImageRendering]。
   >
   >在安装结束时，安装向导将尝试开始图像服务器。 如果未找到有效的许可证密钥，则图像服务器无法开始。 如果存在有效的许可证，并且图像服务器仍未启动，请查阅日志文件。

>[!NOTE]
>
>如果许可证安装完成后安装了图像服务，则必须先手动启动图像服务器，然后才能使用。
