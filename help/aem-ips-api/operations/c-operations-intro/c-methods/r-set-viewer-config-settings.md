---
description: 將檢視器組態設定附加到資產。 這些可以是檢視器預設集或檢視器的來源資產。
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

將檢視器組態設定附加到資產。 這些可以是檢視器預設集或檢視器的來源資產。

语法

## 授權的使用者型別 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-bcc8c83cc84141e8b1341be9133e8511}

**輸入(setViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetHandle | `xsd:string` | 是 | 資產控點。 |
| 名称 | `xsd:string` | 是 | 資產名稱。 |
| 类型 | `xsd:string` | 是 | 您要套用檢視器設定的資產型別。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | 陣列 `ConfigSettings` 已套用至資產…… |

**輸出(setViewerConfigSettingsParam)**

IPS API未傳回此作業的回應。
