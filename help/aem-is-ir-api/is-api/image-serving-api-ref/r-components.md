---
description: 'Scene 7图像提供包含以下组件 '
solution: Experience Manager
title: 图像提供组件
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---

# 图像提供组件{#image-serving-components}

Scene 7图像提供包含以下组件：

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>服务器管理员 </p> </td> 
   <td colname="col2"> <p>负责启动、停止和确保其他组件运行正常的独立可执行文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>为大多数基于Java的组件提供环境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>监控/警报服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 提供服务器监控和电子邮件警报。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平台服务器 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理客户端连接、日志记录、与其他组件的通信。 位于<span class="filepath"> /is/image</span>的HTTP访问。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>缓存服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理Platform Server的数据缓存。 位于/is/cache的HTTP访问。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>图像服务器 </p> </td> 
   <td colname="col2"> <p>执行所有图像处理和图像文件I/O操作。 32位和64位可执行文件都可用于Linux（仅适用于Windows的32位可执行文件）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文本渲染组件 </p> </td> 
   <td colname="col2"> <p>运行<span class="codeph"> textPs=</span>操作时，文本渲染服务的一个或多个实例可能处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG渲染组件 </p> </td> 
   <td colname="col2"> <p>独立的Java应用程序（不由Tomcat托管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media图像渲染(即， 渲染服务器) </p> </td> 
   <td colname="col2"> <p>需要单独的许可证才能激活。 位于<span class="filepath"> /ir/render</span>的HTTP访问。 所有图像渲染功能都集成到平台服务器和图像服务器中，没有单独的可执行组件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

默认目录([!DNL default.ini])或特定图像目录（有关详细信息，请参阅[图像目录](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)）提供了其他配置设置。
