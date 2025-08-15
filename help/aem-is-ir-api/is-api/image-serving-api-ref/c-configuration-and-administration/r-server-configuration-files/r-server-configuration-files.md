---
title: 服务器配置文件
description: 所有配置文件都位于install_folder/conf中，并且可以用大多数文本编辑器进行编辑。 重新启动服务器以使更改生效。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 服务器配置文件{#server-configuration-files}

所有配置文件都位于`install_folder/conf`中，并且可以用大多数文本编辑器进行编辑。 重新启动服务器以使更改生效。

>[!NOTE]
>
>大多数服务器配置文件包含本文档未描述的其他属性和值。 此类属性供内部服务器使用，除非得到Dynamic Media技术支持的指示，否则不得对其进行修改。

本文档讨论以下配置文件的设置：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>配置文件</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>服务器主管配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>目录服务配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>服务器监控配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>图像服务器配置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本文档稍后将更详细地讨论配置文件。
