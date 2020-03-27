---
description: 在服务器上运行的作业。 此外，它还是计划作业的实例。
seo-description: 在服务器上运行的作业。 此外，它还是计划作业的实例。
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

在服务器上运行的作业。 此外，它还是计划作业的实例。

Job存在于3个状态中：

* 计划运行。
* 当前正在运行。
* 已完成运行（并已将信息写入作业日志）。

指定作业类型值以返回作业类型。 您可以返回以下作业：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## 参数 {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 公司 <span class="varname"> 句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 处理公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 作 <span class="varname"> 业处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 处理工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 作业的唯一名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 原 <span class="varname"> 始名称</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">随作业一起提 <span class="codeph"> 交的</span> ActiveJob类型的原始名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 类型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系统返回的作业类型选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 状态</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 系统返回的活动作业状态的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> submitUserEmail <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 安排作业的用户的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">作业日志详细信息和电子邮件本地化的区域设置。 <p>将区域设置指定为 <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>，其中语言代码是ISO-639指定的小写双字母代码，可选国家／地区代码是ISO-3166指定的大写双字母代码。 例如，英语（美国）的区域设置字符串为： <span class="codeph"> 美国</span>。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 说 <span class="varname"> 明</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">最初在submitJob中指定的作 <span class="codeph"> 业说明</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 服 <span class="varname"> 务器名</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 运行作业的服务器的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 开 <span class="varname"> 始日期</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 活动作业的日期、时间和时区。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 总 <span class="varname"> 大小</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 活动作业的总大小。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 进 <span class="varname"> 度</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 作业进度（即作业距完成的距离）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> progress <span class="varname"> 消息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 描述作业进度的文本消息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次进度更新的日期、时间和时区。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TaskProgressArray</span> </td> 
   <td colname="col3"> 异步任务进度信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 图 <span class="varname"> 像服务发布作业</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 图像服务发布作业的作业详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 图 <span class="varname"> 像ServingRenderJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingRenderJob</span> </td> 
   <td colname="col3"> 图像渲染发布作业的作业详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> videoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VideoPublishJob</span> </td> 
   <td colname="col3"> 视频发布作业的作业详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 服务器目录发布作业的作业详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 传UrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> 上传URL作业的作业详细信息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 优 <span class="varname"> 化ImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 重 <span class="varname"> 新处理AssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 传PostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：UploadPostJob</span> </td> 
   <td colname="col3"> 作业详细信息跟踪桌面上传。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ExportJob</span> </td> 
   <td colname="col3">允许授权导出以前上传的文件。 请参阅 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> 导出作业</a>。 </td> 
  </tr> 
 </tbody> 
</table>

