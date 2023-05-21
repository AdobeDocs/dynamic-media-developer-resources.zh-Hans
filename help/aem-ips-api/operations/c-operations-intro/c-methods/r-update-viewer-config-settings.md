---
description: 更新SWF檢視器組態設定。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

更新SWF檢視器組態設定。

语法

## 授權的使用者型別 {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-29790d933fb24aa392d0cb2d52d1310f}

**輸入(updateViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetHandle | `xsd:string` | 是 | 資產控點。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 您要套用至檢視器的組態設定陣列。 |

**輸出(updateViewerConfigSettingsReturn)**

IPS API未傳回此作業的回應。
