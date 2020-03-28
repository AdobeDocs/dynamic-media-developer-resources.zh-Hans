---
description: 更新SWF查看器配置设置。
seo-description: 更新SWF查看器配置设置。
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 资产句柄。 |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | 是 | 要应用于查看器的配置设置的数组。 |

**输出(updateViewerConfigSettingsReturn)**

IPS API不返回此操作的响应。
