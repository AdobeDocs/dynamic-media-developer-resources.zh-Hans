---
description: 将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。
seo-description: 将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

---


# setViewerConfigSettings{#setviewerconfigsettings}

将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。

语法

## 授权用户类型{#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-bcc8c83cc84141e8b1341be9133e8511}

**输入(setViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`name`*` | `xsd:string` | 是 | 资产名称。 |
| `*`类型`*` | `xsd:string` | 是 | 要将查看器配置应用到的资产类型。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 应用于资产的`ConfigSettings`数组。 |

**输出(setViewerConfigSettingsParam)**

IPS API不返回此操作的响应。
