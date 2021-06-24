---
description: 所有配置文件都位于install_folder/conf中，并且大多数文本编辑器都可编辑。 可能需要重新启动服务器才能使更改生效。
solution: Experience Manager
title: 服务器配置文件
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 服务器配置文件{#server-configuration-files}

所有配置文件都位于install_folder/conf中，并且大多数文本编辑器都可编辑。 可能需要重新启动服务器才能使更改生效。

>[!NOTE]
>
>大多数服务器配置文件都包含其他属性和值，本文档中未对这些属性和值进行说明。 此类属性供内部服务器使用，除非Dynamic Media技术支持部门特别指示，否则不得修改。

本文档讨论了以下配置文件的设置：

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
   <td> <p>平台服务器配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>目录服务配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>服务器监视配置。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>图像服务器配置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本文档后面将详细讨论这些配置文件。
