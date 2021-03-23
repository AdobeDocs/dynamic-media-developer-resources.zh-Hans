---
description: 所有配置文件都位于install_folder/conf中，大多数文本编辑器都可编辑。 可能需要重新启动服务器才能使更改生效。
solution: Experience Manager
title: 服务器配置文件
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 服务器配置文件{#server-configuration-files}

所有配置文件都位于install_folder/conf中，大多数文本编辑器都可编辑。 可能需要重新启动服务器才能使更改生效。

>[!NOTE]
>
>大多数服务器配置文件都包含其他属性和值，本文档中未说明这些属性和值。 此类属性仅供内部服务器使用，除非得到Dynamic Media技术支持的特别指示，否则不得进行修改。

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
   <td> <p>服务器管理器配置。 </p> </td> 
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
   <td> <p>映像服务器配置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

配置文件将在本文档的后面更详细地讨论。
