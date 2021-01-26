---
description: 计划运行的作业。
seo-description: 计划运行的作业。
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Dynamic Media Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

计划运行的作业。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司手柄。 |
| `*`jobHandle`*` | `xsd:string` | 计划的作业处理。 |
| `*`name`*` | `xsd:string` | 作业名称. |
| `*`originalName`*` | `xsd:string` | 计划作业的原始名称。 |
| `*`类型`*` | `xsd:string` | 作业类型。 |
| `*`submitUserEmail`*` | `xsd:string` | 调度作业的用户的电子邮件地址。 |
| `*`locale`*` | `xsd:string` | 用于作业日志详细信息和电子邮件本地化的区域设置。 区域设置指定为`<language_code>[- <country_code>]`，其中语言代码是ISO-639指定的小写、双字母代码，可选国家／地区代码是ISO-3166指定的大写、双字母代码。 例如，英语（美国）的区域设置字符串为：`en-US`。 |
| `*`描述`*` | `xsd:string` | 最初在`submitJob`中指定的作业描述。 |
| `*`execSchedule`*` | `xsd:string` | 作业计划运行的时间。 |
| `*`nextFireTime`*` | `xsd:dateTime` | 作业被激发的日期、时间和时区。 |
| `*`时区`*` | `xsd:dateTime` | 计划作业的时区。 |
| `*`triggerState`*` | `xsd:int` | 选择作业触发状态。 |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | 图像服务发布作业的作业详细信息。 |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | 图像渲染作业的作业详细信息。 |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | 视频发布作业的作业详细信息。 请参阅[ VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | 服务器目录发布作业的作业详细信息。 |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | 上载目录作业的作业详细信息。 |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | 上传URL作业的作业详细信息。 |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | 允许授权导出以前上传的文件。 请参阅[导出作业](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |

## 说明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

当您在`submitJob`中指定作业类型值时，系统将返回基于该类型的作业。 可以返回以下作业：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

