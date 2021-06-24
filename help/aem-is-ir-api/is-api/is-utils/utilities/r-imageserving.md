---
description: 图像提供控制脚本。 此脚本用于启动、停止或重新启动图像服务服务器管理器，而映像服务服务器管理器又启动、停止或重新启动所有其他图像服务组件。
solution: Experience Manager
title: 图像服务
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# 图像服务{#imageserving}

图像提供控制脚本。 此脚本用于启动、停止或重新启动图像服务服务器管理器，而映像服务服务器管理器又启动、停止或重新启动所有其他图像服务组件。

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
   <td colname="col2"> <p> 启动服务器管理员和所有其他图像服务组件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> 停止所有图像服务组件，包括服务器管理员。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动 </span> </p> </td> 
   <td colname="col2"> <p>重新启动所有映像服务组件，包括服务器管理员。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动 |表示 | svg }  </span> </p> </td> 
   <td colname="col2"> <p> 重新启动Tomcat/Platform服务器、图像服务器或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 状态[ ps |表示 | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>返回图像服务器、Tomcat/Platform Server和SVGserver的正常运行时间和当前内存使用信息，或仅返回指定服务器的状态；如果服务器管理员未运行，则会返回信息性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>
