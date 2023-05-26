---
description: 特定于公司的配置设置。
solution: Experience Manager
title: 公司设置
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

特定于公司的配置设置。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| overwriteMode | `xsd:string` | 确定是否使用相同的基本图像名称和扩展名覆盖当前文件夹中的图像。 |
| retainPublishState | `xsd:boolean` | 指定上载到IPS的替换图像是保留现有的“发布准备就绪”设置，还是按上载指定。 |
| defaultsourceprofile | `types:Asset` | 指定在添加CMYK图像文件时作为“使用默认颜色行为”的一部分自动应用的默认源颜色配置文件(涂层的FOGRA27 (ISO 126472：2004))。 |
| defaultdisplayprofile | `types:Asset` | 指定在添加CMYK图像文件时作为“使用默认颜色行为”的一部分自动应用的默认内部颜色配置文件(U.S. Web Coated (SWOP) v2)。 |
| iptcExifMappingXslt | `types:Asset` | 将IPTC和EXIF图像头数据提取到IPS需要从内部字段名称转换为公司用户定义的字段名称。 确定已上传图像的XSL转换表（默认为“不提取任何IPTC或EXIF字段”）。 |
| xmpMappingXslt | `types:Asset` | 将XMP图像头数据提取到IPS需要从内部字段名称转换为公司用户定义的字段名称。 确定已上传图像的XSL翻译表(默认为“不提取任何XMP字段”)。 |
| diskSpaceWarningMin | `xsd:int` | 发出警告之前的最小映像目录可用磁盘空间量。 |
| emailTrashCleanupWarning | `xsd:boolean` | 确定在自动删除置入垃圾桶中的项目之前是否发送电子邮件。 |
| javascriptUploadEnable | `types:Asset` | 确定是否上传JavaScript文件。 这是潜在的安全风险，因此请谨慎使用此选项。 |
