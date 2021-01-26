---
description: 包含平台服务器设置。
seo-description: 包含平台服务器设置。
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# server.xml{#server-xml}

包含平台服务器设置。

修改此XML文件时，必须注意保持有效的XML语法，否则平台服务器可能无法开始。

要使更改生效，必须在编辑此文件后重新启动平台服务器。

下图说明了在此文件中可更改的设置。 请参阅本文档前面的相应部分，以了解这些设置的说明。 请注意，此图不是[!DNL server.xml]的完整表示形式。

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

