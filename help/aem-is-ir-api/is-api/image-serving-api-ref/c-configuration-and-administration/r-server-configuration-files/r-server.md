---
description: 包含平台伺服器設定。
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

包含平台伺服器設定。

修改此XML檔案時，必須注意維護有效的XML語法，否則 [!DNL Platform Server] 可能無法啟動。

若要讓變更生效， [!DNL Platform Server] 編輯此檔案後必須重新啟動。

下圖說明哪些設定可以在此檔案中變更。 如需這些設定的說明，請參閱本檔案前面對應的章節。 請注意，此圖表並不完全代表 [!DNL server.xml].

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
