---
description: 图像服务控制脚本。 此脚本用于启动、停止或重新启动图像服务服务器主管，进而启动、停止或重新启动所有其他图像服务组件。
solution: Experience Manager
title: Imageserving
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# Imageserving{#imageserving}

图像服务控制脚本。 此脚本用于启动、停止或重新启动图像服务服务器主管，进而启动、停止或重新启动所有其他图像服务组件。

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
   <td colname="col2"> <p> 启动“服务器监控器”和所有其他图像服务组件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止 </span> </p> </td> 
   <td colname="col2"> <p> 停止所有图像服务组件，包括服务器监控程序。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动 </span> </p> </td> 
   <td colname="col2"> <p>重新启动所有图像服务组件，包括服务器监控程序。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动{ ps |是 | svg } </span> </p> </td> 
   <td colname="col2"> <p> 重新启动Tomcat/[!DNL Platform Server]、图像服务器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 状态[ ps |是 | svg ] </span> </p> </td> 
   <td colname="col2"> <p>返回图像服务器Tomcat/的正常运行时间和当前内存使用信息[!DNL Platform Server]和SVGserver，或仅指定服务器的状态；如果服务器监控器未运行，则返回信息性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
