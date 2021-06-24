---
description: 向系统提交作业。
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 11%

---

# submitJob{#submitjob}

向系统提交作业。

语法

## 授权用户类型 {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-31a07dbccf964850883e817384499459}

**输入(submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>公司负责人。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>处理提交作业的用户。 </p> <p> <p>注意：系统会向<span class="codeph"> userHandle</span>指定的用户发送电子邮件。 如果未提供<span class="codeph"> userHandle</span>，则提交工作的人员会收到电子邮件。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>作业名称. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>用于作业日志详细信息和电子邮件本地化的区域设置。 </p> <p>区域设置指定为<span class="codeph"> &lt;languagecode&gt;</span>和<span class="codeph"> [&lt;countrycode&gt;]</span>，其中语言代码是ISO-639指定的小写字母、双字母代码，而可选国家/地区代码是ISO-3166指定的大写双字母代码。 例如，英语（美国）的区域设置字符串将为：美国。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>运行作业的日期和时间。 </p> <p>注意： 为时区提供请求。 时区将调整为目标IPS服务器的时区。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>确定运行作业的时间。 </p> <p> 可以是运行定期作业的<span class="codeph"> cron</span>字符串。 </p> <p>计划始终与服务器的本地时区相关。 有关自定义计划格式，请参阅IPS文档。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 描述</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>作业描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ExportJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>导出以前上传的文件。 </p> <p>请参阅<a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ImageServingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>提供发布作业的图像的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>有关图像渲染发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VideoPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>视频发布作业的详细信息。 </p> <p>请参阅<a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>服务器目录发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：UploadDirectoryJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上载目录作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：UploadUrlsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上传URL作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：OptimizeImagesJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：RipPdfsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：ReprocessAssetsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>使用自动设置脚本将资产列表处理为多个集。 </p> <p>请参阅<a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(submitJobReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobHandle`*` | `xsd:string` | 是 | 作业处理。 |

## 示例 {#section-40ac77d14adf4588ba2575be6879b2d2}

此代码示例将提供发布作业的图像提交到IPS并返回作业句柄。 请求中只选择一种类型的作业。 由于`userHandle`被忽略，因此会向提交作业的用户发送电子邮件通知。 此示例作业会立即运行，因为忽略了`execTime`和`execSchedule`。

**请求**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**响应**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## 说明 {#section-0f3078e503a249aeb6f3d662a51f036a}

您最多可以指定`execTime`和`execSchedule`中的任一值。 如果两者均未传递，则作业会立即运行。 您只能使用以下任一项：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
