---
description: 特定于公司的配置设置。
solution: Experience Manager
title: 公司设置
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 2%

---

# 公司设置{#companysettings}

特定于公司的配置设置。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | 确定是否使用相同的基本图像名称和扩展名覆盖当前文件夹中的图像。 |
| `*`retainPublishState`*` | `xsd:boolean` | 指定上传到IPS的替换图像是应保留现有的“准备发布”设置，还是应按照上传指定的方式进行。 |
| `*`defaultSourceProfile`*` | `types:Asset` | 指定在添加CMYK图像文件时自动作为“使用默认颜色行为”一部分应用的默认源颜色配置文件(Coated FOGRA27(ISO 126472:2004))。 |
| `*`defaultDisplayProfile`*` | `types:Asset` | 指定在添加CMYK图像文件时，自动作为“使用默认颜色行为”的一部分应用的默认内部颜色配置文件(US Web Coated(SWOP)v2)。 |
| `*`iptcExifMappingXslt`*` | `types:Asset` | 将IPTC和EXIF图像标头数据提取到IPS中，需要将公司的内部字段名称转换为用户定义的字段名称。 为上传的图像确定XSL转换表（默认为“不提取任何IPTC或EXIF字段”）。 |
| `*`xmpMappingXslt`*` | `types:Asset` | 要将XMP图像头数据提取到IPS，需要将公司的内部字段名称转换为用户定义的字段名称。 为上传的图像确定XSL转换表(默认为“不提取任何XMP字段”)。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 发出警告之前映像目录可用磁盘空间的最小数量。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | 确定是否在放入垃圾桶的项目自动删除之前发送电子邮件。 |
| `*`javascriptUploadEnabled`*` | `types:Asset` | 确定是否上传JavaScript文件。 这存在潜在的安全风险，因此请谨慎使用此选项。 |
