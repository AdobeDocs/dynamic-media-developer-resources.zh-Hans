---
title: 图像服务组件
description: Dynamic Media图像服务包含以下组件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 图像服务组件{#image-serving-components}

Dynamic Media图像服务包含以下组件：

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>组件 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>服务器主管 </p> </td> 
   <td colname="col2"> <p>一个独立的可执行文件，负责启动、停止并确保其他组件的健康。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>它为大多数基于Java的组件提供了环境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>监控/警报服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 提供服务器监控和电子邮件警报。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理客户端连接、日志记录以及与其他组件的通信。 HTTP访问 <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>缓存服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理 [!DNL Platform Server]的数据缓存。 /is/cache上的HTTP访问。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>图像服务器 </p> </td> 
   <td colname="col2"> <p>它执行所有图像处理和图像文件I/O操作。 32位和64位可执行文件均适用于Linux®（32位仅适用于Windows）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文本渲染组件 </p> </td> 
   <td colname="col2"> <p>文本渲染服务的一个或多个实例可能在以下情况下处于活动状态： <span class="codeph"> textPs=</span> 运行操作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG渲染组件 </p> </td> 
   <td colname="col2"> <p>独立的Java™应用程序（不由Tomcat托管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dynamic Media图像渲染(又称 渲染服务器) </p> </td> 
   <td colname="col2"> <p>它需要单独的许可证才能激活。 HTTP访问 <span class="filepath"> /ir/render</span>. 所有图像渲染功能都已集成到 [!DNL Platform Server] 和图像服务器，没有单独的可执行组件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

默认目录( [!DNL default.ini])或特定图像目录(请参阅 [图像目录](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) 以了解详情)。
