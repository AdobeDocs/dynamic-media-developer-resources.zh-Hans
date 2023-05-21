---
description: 所有組態檔案都位於install_folder/conf中，並且可以用大多數的文字編輯器進行編輯。 伺服器可能需要重新啟動才能讓變更生效。
solution: Experience Manager
title: 伺服器組態檔
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# 伺服器組態檔{#server-configuration-files}

所有組態檔案都位於install_folder/conf中，並且可以用大多數的文字編輯器進行編輯。 伺服器可能需要重新啟動才能讓變更生效。

>[!NOTE]
>
>大部分的伺服器組態檔都包含本檔案未說明的其他屬性和值。 此類屬性供內部伺服器使用，除非Dynamic Media技術支援部門特別指示，否則不得修改。

本檔案討論下列組態檔的設定：

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>組態檔</b> </th> 
   <th class="entry"> <b>说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>伺服器監督員組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] 配置. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>目錄服務設定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>伺服器監視組態。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>影像伺服器設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

本檔案稍後會更詳細地討論組態檔。
