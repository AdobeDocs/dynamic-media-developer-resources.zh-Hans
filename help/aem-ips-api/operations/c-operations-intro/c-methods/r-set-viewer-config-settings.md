---
description: 将查看器配置设置附加到资产。 这些可以是查看器预设或查看器的源资产。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

将查看器配置设置附加到资产。 这些可以是查看器预设或查看器的源资产。

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
| companyHandle | `xsd:string` | 是 | 处理公司。 |
| assetHandle | `xsd:string` | 是 | 资源句柄。 |
| 名称 | `xsd:string` | 是 | 资源名称。 |
| 类型 | `xsd:string` | 是 | 要将查看器配置应用于的资源类型。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 数组 `ConfigSettings` 应用于资产…… |

**输出(setViewerConfigSettingsParam)**

IPS API未返回此操作的响应。
