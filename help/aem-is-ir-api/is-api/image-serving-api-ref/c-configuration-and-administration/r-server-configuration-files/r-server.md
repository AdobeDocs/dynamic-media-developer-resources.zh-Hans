---
description: 包含平台服务器设置。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

包含平台服务器设置。

修改此XML文件时，必须注意保持有效的XML语法，否则平台服务器可能无法开始。

要使更改生效，必须在编辑此文件后重新启动平台服务器。

下图说明了可在此文件中更改的设置。 有关这些设置的说明，请参阅本文档前面的相应部分。 请注意，此图不是[!DNL server.xml]的完整表示形式。

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

