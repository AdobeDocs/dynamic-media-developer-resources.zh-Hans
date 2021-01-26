---
description: 获取与指定资产关联的所有查看器配置设置。
seo-description: 获取与指定资产关联的所有查看器配置设置。
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 18%

---


# getViewerConfigSettings{#getviewerconfigsettings}

获取与指定资产关联的所有查看器配置设置。

语法

## 授权用户类型{#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**输入(getViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理资产。 |

**输出(getViewerConfigSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`类型`*` | `xsd:string` | 是 | 应用配置设置的查看器类型。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | 是 | 查看器配置设置的数组。 |

