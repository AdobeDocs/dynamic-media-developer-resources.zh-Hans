---
description: 计划运行的作业。
solution: Experience Manager
title: 计划作业
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
TQID: 'https://experienceleague.adobe.com/OFG30nHlkuRT7HeNob0hkEfaygi8b2gNFEiu67LJBmU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 3%

---

# [!DNL ScheduledJob]{#scheduledjob}

计划运行的作业。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司句柄。 |
| jobHandle | `xsd:string` | 计划的作业句柄。 |
| 名称 | `xsd:string` | 作业名称。 |
| 原始名称 | `xsd:string` | 计划作业的原始名称。 |
| 类型 | `xsd:string` | 作业类型。 |
| submitUserEmail | `xsd:string` | 安排作业的用户的电子邮件地址。 |
| 区域设置 | `xsd:string` | 用于作业日志详细信息和电子邮件本地化的区域设置。 区域设置指定为`<language_code>[- <country_code>]`，其中语言代码是ISO-639指定的小写双字母代码，而可选国家/地区代码是ISO-3166指定的大写双字母代码。 例如，英语（美国）的区域设置字符串应为： `en-US`。 |
| description | `xsd:string` | 最初在`submitJob`中指定的作业的描述。 |
| execSchedule | `xsd:string` | 作业计划运行的时间。 |
| nextFireTime | `xsd:dateTime` | 作业触发的日期、时间和时区。 |
| 时区 | `xsd:dateTime` | 计划作业的时区。 |
| triggerState | `xsd:int` | 作业触发器状态的选择。 |
| imageServingPublishJob | `types:ImageServingPublishJob` | 图像服务发布作业的作业详细信息。 |
| imageServingRenderJob | `types:ImageServingRenderJob` | 图像渲染作业的作业详细信息。 |
| videoPublishJob | `types:VideoPublishJob` | 视频发布作业的作业详细信息。 查看[VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | 服务器目录发布作业的作业详细信息。 |
| 上载目录作业 | `types:UploadDirectoryJob` | 上载目录作业的作业详细信息。 |
| uploadUrlsJob | `types:UploadUrlsJob` | 上载URL作业的作业详细信息。 |
| optimizeImageJob | `types:OptimizeImagesJob` | |
| ripPdfJob | `types:RipPdfsJob` | |
| reprocessAssets作业 | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | 允许授权导出以前上载的文件。 请参阅[导出作业](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html)。 |

## 说明 {#section-34ec157f281f412f9f0f6e861e6ed0cd}

当您在`submitJob`中指定作业类型值时，系统会根据该类型返回作业。 可以返回以下作业：

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

