---
description: 获取与指定资产关联的所有查看器配置设置。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic，SDK/API，查看器预设
role: Developer,Administrator
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

获取与指定资产关联的所有查看器配置设置。

语法

## 授权用户类型 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**输入(getViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理资产。 |

**输出(getViewerConfigSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`类型`*` | `xsd:string` | 是 | 应用配置设置的查看器类型。 |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | 是 | 查看器配置设置的数组。 |
