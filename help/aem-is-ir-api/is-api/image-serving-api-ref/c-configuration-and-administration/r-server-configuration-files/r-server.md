---
description: 包含平台服务器设置。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

包含平台服务器设置。

修改此XML文件时，必须注意维护有效的XML语法，否则平台服务器可能无法启动。

要使更改生效，必须在编辑此文件后重新启动Platform Server。

下图说明了此文件中可更改的设置。 有关这些设置的说明，请参阅本文档前面的相应章节。 请注意，此图不是[!DNL server.xml]的完整表示形式。

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```
