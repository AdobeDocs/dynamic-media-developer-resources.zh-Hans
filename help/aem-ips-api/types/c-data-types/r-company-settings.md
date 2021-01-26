---
description: 公司特定的配置设置。
seo-description: 公司特定的配置设置。
seo-title: 公司设置
solution: Experience Manager
title: 公司设置
topic: Dynamic Media Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 2%

---


# CompanySettings{#companysettings}

公司特定的配置设置。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | 确定是否使用相同的基本图像名称和扩展名覆盖当前文件夹中的图像。 |
| `*`retainPublishState`*` | `xsd:boolean` | 指定上传到IPS的替换图像是否应保留现有的“准备发布”设置，或是否应按照上传指定的方式进行发布。 |
| `*`defaultSourceProfile`*` | `types:Asset` | 指定在添加CMYK图像文件时自动应用作为“使用默认颜色行为”一部分的默认源颜色用户档案(Coated FOGRA27(ISO 126472:2004))。 |
| `*`defaultDisplayProfile`*` | `types:Asset` | 指定在添加CMYK图像文件时自动作为“使用默认颜色行为”的一部分应用的默认内部颜色用户档案(U.S. Web Coated(SWOP)v2)。 |
| `*`iptcExifMappingXslt`*` | `types:Asset` | 将IPTC和EXIF图像头提取转换为IPS时，需要将公司从内部字段名称转换为用户定义的字段名称。 为上传的图像确定XSL转换表（默认为“不提取任何IPTC或EXIF字段”）。 |
| `*`xmpMappingXslt`*` | `types:Asset` | 将XMP图像头数据提取到IPS时，需要将公司从内部字段名称转换为用户定义的字段名称。 为上传的图像确定XSL转换表(默认为“不提取任何XMP字段”)。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 发出警告前映像目录可用磁盘空间的最小数量。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | 确定是否在自动删除放入垃圾桶的物品之前发送电子邮件。 |
| `*`javascriptUploadEnabled`*` | `types:Asset` | 确定是否上传JavaScript文件。 这是潜在的安全风险，因此请谨慎使用此选项。 |

