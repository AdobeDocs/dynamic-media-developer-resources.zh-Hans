---
description: 更新SWF查看器配置设置。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic，SDK/API，查看器预设
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 13%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF查看器配置设置。

语法

## 授权用户类型{#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-29790d933fb24aa392d0cb2d52d1310f}

**输入(updateViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 要应用到查看器的配置设置的数组。 |

**输出(updateViewerConfigSettingsReturn)**

IPS API不返回此操作的响应。
