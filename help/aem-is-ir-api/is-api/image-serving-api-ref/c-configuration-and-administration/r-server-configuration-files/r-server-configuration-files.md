---
title: 服务器配置文件
description: 所有配置文件都位于install_folder/conf中，并且可以用大多数文本编辑器进行编辑。 重新启动服务器以使更改生效。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
TQID: 'https://experienceleague.adobe.com/Gp1W--QzWptazkc1ygnmw59lO8zrNmgmabYMOz8jUG4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 133
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
