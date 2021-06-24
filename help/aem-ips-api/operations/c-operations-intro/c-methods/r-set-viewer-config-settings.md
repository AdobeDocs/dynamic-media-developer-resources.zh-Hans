---
description: 将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic，SDK/API，查看器预设
role: Developer,Administrator
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。

语法

## 授权用户类型 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-bcc8c83cc84141e8b1341be9133e8511}

**输入(setViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`name`*` | `xsd:string` | 是 | 资产名称。 |
| `*`类型`*` | `xsd:string` | 是 | 要将查看器配置应用到的资产类型。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 应用于资产的`ConfigSettings`数组。 |

**输出(setViewerConfigSettingsParam)**

IPS API不会返回此操作的响应。
