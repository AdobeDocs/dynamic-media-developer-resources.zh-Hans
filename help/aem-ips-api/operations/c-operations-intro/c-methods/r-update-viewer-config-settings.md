---
description: 更新SWF查看器配置设置。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic，SDK/API，查看器预设
role: Developer,Administrator
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF查看器配置设置。

语法

## 授权用户类型 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-29790d933fb24aa392d0cb2d52d1310f}

**输入(updateViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 要应用于查看器的配置设置的数组。 |

**Output(updateViewerConfigSettingsReturn)**

IPS API不会返回此操作的响应。
