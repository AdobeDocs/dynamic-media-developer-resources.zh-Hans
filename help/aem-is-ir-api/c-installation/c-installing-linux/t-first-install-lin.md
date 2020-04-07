---
description: 此过程说明如何首次在Linux上安装图像服务。
seo-description: 此过程说明如何首次在Linux上安装图像服务。
seo-title: 首次安装
solution: Experience Manager
title: 首次安装
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 首次安装{#installing-for-the-first-time}

此过程说明如何首次在Linux上安装图像服务。

1. 使用根权限登录到服务器主机。
1. 创建文件夹 [!DNL /usr/local/scene7/licenses]。

   如果图像服务和／或图像渲染许可证密钥文件(带 [!DNL .sc8] 有文件后缀)可用，请将其复制到此文件夹。 否则，请继续安装，稍后再安装许可证密钥。
1. 解压缩和解压缩图像服务分发tar文件。
1. 运 [!DNL ./install-is]行(位于文件夹 [!DNL Setup] 中)以启动安装向导。
   如果未找到许可证密钥，则显示说明如何获取许可证文件。 此时执行此操作，或继续安装图像服务，稍后再安装许可证密钥。
1. 当显示最终用户许可协议(EULA)时，请阅读许可协议，然后输 `y` 入以继续。

   安装程序显示下表中列出的提示。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 主监听端口[8080]:</span> </p> </td> 
   <td colname="col2"> <p>用于图像服务和图像渲染的主HTTP监听端口。 </p> </td> 
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
   <td colname="col2"> <p>要安装图像服务器的用户帐户。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 图像服务器组ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>要安装图像服务器的组帐户。 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. 按 **[!UICONTROL Enter]** 以接受默认值或指定其他值。

   确保指定的所有端口号都是唯一的，并且此主机上不会使用它。

   **重要：**如果指定了除根帐户之外的帐户，则必须确保在配置文件中重新配置这些文件夹时正确设置了图像服务器需要读取和／或写入的所有文件和文件夹的访问权限。
>图像服务现已安装到 [!DNL /usr/local/Scene7/ImageServing]。 某些图像渲染内容已安装到 [!DNL /usr/local/Scene7/ImageRendering]。
>
>在安装结束时，安装向导将尝试开始图像服务器。 如果未找到有效的许可证密钥，则图像服务器将无法开始。 如果存在有效的许可证，并且图像服务器仍未启动，请查阅日志文件。
>[!NOTE]
如果许可证是在安装图像服务后安装的，则必须先手动启动图像服务器，然后才能使用。
>
>
>

