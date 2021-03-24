---
description: 将查看器配置设置附加到资产。 这些预设可以是查看器预设，也可以是查看器的源资产。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic，SDK/API，查看器预设
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 11%

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

**Input(setViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`name`*` | `xsd:string` | 是 | 资产名称。 |
| `*`类型`*` | `xsd:string` | 是 | 要将查看器配置应用到的资产类型。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 应用到资产的`ConfigSettings`数组。 |

**输出(setViewerConfigSettingsParam)**

IPS API不返回此操作的响应。
