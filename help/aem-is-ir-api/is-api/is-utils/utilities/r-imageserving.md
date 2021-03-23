---
description: 图像服务控制脚本。 此脚本用于开始、停止或重新启动图像服务服务器管理器，而后者又会开始、停止或重新启动所有其他图像服务组件。
seo-description: 图像服务控制脚本。 此脚本用于开始、停止或重新启动图像服务服务器管理器，而后者又会开始、停止或重新启动所有其他图像服务组件。
seo-title: 图像服务
solution: Experience Manager
title: 图像服务
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# ImageServing{#imageserving}

图像服务控制脚本。 此脚本用于开始、停止或重新启动图像服务服务器管理器，而后者又会开始、停止或重新启动所有其他图像服务组件。

## 使用 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`命令`*`

## 命令{#section-90436a0b0f70435f9ac42dafeed2c17b}

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
   <td colname="col2"> <p> 开始服务器管理器和所有其他图像服务组件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 停止  </span> </p> </td> 
   <td colname="col2"> <p> 停止所有图像服务组件，包括服务器管理器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动 </span> </p> </td> 
   <td colname="col2"> <p>重新启动所有映像服务组件，包括服务器管理器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重新启动 | | svg }  </span> </p> </td> 
   <td colname="col2"> <p> 重新启动Tomcat/Platform Server、Image Server或SVG。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 状态[ ps | | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>返回Image Server、Tomcat/Platform Server和SVGserver的正常运行时间和当前内存使用信息，或仅指定服务器的状态；如果服务器主管未运行，则返回信息性消息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

