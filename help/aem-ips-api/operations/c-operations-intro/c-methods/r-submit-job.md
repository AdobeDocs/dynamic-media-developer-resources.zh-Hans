---
description: 向系统提交作业。
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 11%

---


# submitJob{#submitjob}

向系统提交作业。

语法

## 授权用户类型{#section-eb7024277bec43c79e03f396205be16f}

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
   <td colname="col4"> <p>公司手柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>处理提交作业的用户。 </p> <p> <p>注意：系统会向由<span class="codeph"> userHandle</span>指定的用户发送电子邮件。 如果未提供<span class="codeph"> userHandle</span>，则提交作业的人员会收到电子邮件。 </p> </p> </td> 
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
   <td colname="col4"> <p>用于作业日志详细信息和电子邮件本地化的区域设置。 </p> <p>区域设置指定为<span class="codeph"> &lt;languagecode&gt;</span>和<span class="codeph"> [&lt;countrycode&gt;]</span>，其中语言代码为ISO-639指定的小写、双字母代码，可选国家/地区代码为ISO-3166指定的大写、双字母代码。 例如，英语（美国）的区域设置字符串为：en-US。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>运行作业的日期和时间。 </p> <p>注意： 为请求提供时区。 时区将调整为目标 IPS服务器的时区。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>确定何时运行作业。 </p> <p> 可以是循环运行作业的<span class="codeph"> cron</span>字符串。 </p> <p>计划始终与服务器的本地时区相关。 有关自定义计划格式，请参阅IPS文档。 </p> </td> 
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
   <td colname="col4"> <p>图像服务发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>图像渲染发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：VideoPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>视频发布作业的详细信息。 </p> <p>请参阅<a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>服务器目录发布作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadDirectoryJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上载目录作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UploadUrlsJob</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>上载URL作业的详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:OptimizeImagesJob</span> </td> 
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
   <td colname="col2"> <span class="codeph"> types:ReprocessAssetsJob</span> </td> 
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
| `*`jobHandle`*` | `xsd:string` | 是 | 工作。 |

## 示例 {#section-40ac77d14adf4588ba2575be6879b2d2}

此代码示例将提供发布作业的图像提交到IPS并返回作业句柄。 请求中只选择一种类型的作业。 由于`userHandle`被省略，电子邮件通知将发送给提交作业的用户。 此示例作业会立即运行，因为省略了`execTime`和`execSchedule`。

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

您最多可以指定`execTime`和`execSchedule`中的一个。 如果两者均未通过，则作业将立即运行。 您只能使用以下任一选项：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

