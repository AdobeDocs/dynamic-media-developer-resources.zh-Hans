---
description: 'Scene 7图像服务由以下组件组成 '
seo-description: 'Scene 7图像服务由以下组件组成 '
seo-title: 图像服务组件
solution: Experience Manager
title: 图像服务组件
topic: Scene7 Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像服务组件{#image-serving-components}

Scene 7图像服务由以下组件组成：

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
   <td colname="col2"> <p>负责启动、停止和确保其他组件运行正常的独立可执行程序。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>为大多数基于Java的组件提供环境。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>监视／警报服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 提供服务器监视和电子邮件警报。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>平台服务器 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理客户端连接、记录、与其他组件的通信。 位于/is/ <span class="filepath"> image的HTTP访问</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>缓存服务 </p> </td> 
   <td colname="col2"> <p>J2EE应用程序。 管理Platform Server的数据缓存。 位于/is/cache的HTTP访问。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>图像服务器 </p> </td> 
   <td colname="col2"> <p>执行所有图像处理和图像文件I/O操作。 32位和64位可执行程序都可用于Linux（仅适用于Windows的32位可执行程序）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE文本渲染组件 </p> </td> 
   <td colname="col2"> <p>当运行textPs=操作时，文本渲染服务的一个或多 <span class="codeph"> 个实例可</span> 以处于活动状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG渲染组件 </p> </td> 
   <td colname="col2"> <p>独立的Java应用程序（不由Tomcat托管）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scene7图像渲染(aka. 渲染服务器) </p> </td> 
   <td colname="col2"> <p>需要单独的许可证才能激活。 位于/ir/ <span class="filepath"> render的HTTP访问</span>。 所有图像渲染功能都集成到平台服务器和图像服务器中，没有单独的可执行组件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

其他配置设置由默认目录( [!DNL default.ini])或特定图像目录提供(有关详细信 [息，请参阅图像目录](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) )。
