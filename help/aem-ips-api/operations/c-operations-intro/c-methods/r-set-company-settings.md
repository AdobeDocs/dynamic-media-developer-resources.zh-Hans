---
description: 设置各种公司特定配置值。
seo-description: 设置各种公司特定配置值。
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Dynamic Media Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 12%

---


# setCompanySettings{#setcompanysettings}

设置各种公司特定配置值。

语法

## 授权用户类型{#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-a472da6c57c74a94a179dda081004888}

**输入(setCompanySettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`overwriteMode`*` | `xsd:string` | 否 | 资产覆盖模式。 |
| `*`retainPublishState`*` | `xsd:boolean` | 否 | 设置为`true`可在重新上传资产时保留发布状态。 |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | 否 | IccProfile资产，用作默认源颜色用户档案。 |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | 否 | 用作默认显示颜色用户档案的IccProfile资产。 |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | 否 | 用于将IPTC和EXIF元数据映射到IPS元数据字段的XSL资源。 |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | 否 | 用于将XMP元数据映射到IPS元数据字段的XSL资源。 |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 否 | 在发送警告消息之前，可用的最小可用磁盘空间（以KB为单位）。 |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | 否 | 设置为`true`，当资源从垃圾桶中清空时，向公司管理员发送通知。 |

**输出(setCompanySettingsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

此代码示例设置公司的配置。

**请求**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**响应**

无。
