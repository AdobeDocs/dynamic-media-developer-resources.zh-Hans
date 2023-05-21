---
description: 影像伺服控制指令碼。 此指令碼可用來啟動、停止或重新啟動「影像伺服伺服器監督員」，進而啟動、停止或重新啟動所有其他的「影像伺服」元件。
solution: Experience Manager
title: ImageServe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# ImageServe{#imageserving}

影像伺服控制指令碼。 此指令碼可用來啟動、停止或重新啟動「影像伺服伺服器監督員」，進而啟動、停止或重新啟動所有其他的「影像伺服」元件。

## 使用 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`命令`*`

## 命令 {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>命令 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 启动 </span> </p> </td> 
   <td colname="col2"> <p> 啟動「伺服器監督員」和所有其他的「影像伺服」元件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止 </span> </p> </td> 
   <td colname="col2"> <p> 停止所有「影像伺服」元件，包括「伺服器監督員」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動 </span> </p> </td> 
   <td colname="col2"> <p>重新啟動所有「影像伺服」元件，包括Server Supervisor。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新啟動{ ps |是 | svg } </span> </p> </td> 
   <td colname="col2"> <p> 重新啟動Tomcat/[!DNL Platform Server]、影像伺服器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 狀態[ ps |是 | svg ] </span> </p> </td> 
   <td colname="col2"> <p>傳回影像伺服器Tomcat/的運作時間和目前記憶體使用量資訊[!DNL Platform Server]和SVGserver，或只有指定伺服器的狀態；如果Server Supervisor未執行，則會傳回資訊性訊息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
