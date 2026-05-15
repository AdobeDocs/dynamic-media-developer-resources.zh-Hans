---
description: 特定于公司的配置设置。
solution: Experience Manager
title: 公司设置
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
TQID: 'https://experienceleague.adobe.com/iGc-AwCFbpkATjLjvSBtx4vsP0-OUDSkH2dFHZ-j2rg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

特定于公司的配置设置。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| overwritemode | `xsd:string` | 确定是否使用相同的基本图像名称和扩展名覆盖当前文件夹中的图像。 |
| retainPublishState | `xsd:boolean` | 指定上载到IPS的替换图像是保留现有的“发布准备就绪”设置，还是使用上载项指定的设置。 |
| defaultsourceprofile | `types:Asset` | 指定在添加CMYK图像文件时作为“使用默认颜色行为”的一部分自动应用的默认源颜色配置文件(涂层的FOGRA27 (ISO 126472:2004))。 |
| defaultDisplayprofile | `types:Asset` | 指定在添加CMYK图像文件时作为“使用默认颜色行为”的一部分自动应用的默认内部颜色配置文件(U.S. Web Coated (SWOP) v2)。 |
| iptcExifMappingXslt | `types:Asset` | 将IPTC和EXIF图像标题数据提取到IPS需要从内部字段名称转换为公司的用户定义的字段名称。 确定已上传图像的XSL翻译表（默认为“不提取任何IPTC或EXIF字段”）。 |
| xmpMappingXslt | `types:Asset` | 将XMP图像标题数据提取到IPS需要从内部字段名称转换为公司的用户定义的字段名称。 确定已上传图像的XSL翻译表（默认为“不提取任何XMP字段”）。 |
| diskSpaceWarningMin | `xsd:int` | 发出警告之前映像目录可用磁盘空间的最小量。 |
| emailTrashCleanupWarning | `xsd:boolean` | 确定在自动删除垃圾桶项目之前是否发送电子邮件。 |
| javascriptuploadenabled | `types:Asset` | 确定是否上传JavaScript文件。 此选项存在潜在安全风险，因此请谨慎使用。 |
