---
description: 所有配置文件都位于install_folder/conf中，并且可以用大多数文本编辑器进行编辑。 可能需要重新启动服务器以使更改生效。
solution: Experience Manager
title: 服务器配置文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# 服务器配置文件{#server-configuration-files}

所有配置文件都位于install_folder/conf中，并且可以用大多数文本编辑器进行编辑。 可能需要重新启动服务器以使更改生效。

>[!NOTE]
>
>大多数服务器配置文件包含本文档未介绍的其他属性和值。 此类属性供内部服务器使用，除非Dynamic Media技术支持人员特别说明，否则不得修改。

本文档讨论以下配置文件的设置：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>配置文件</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>服务器监控器配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 配置. </p> </td> 
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
