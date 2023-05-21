---
description: 僅供內部使用。 使用者應該參考影像伺服影像目錄參考 — 屬性參考區段。
solution: Experience Manager
title: getimageservingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 16%

---

# getimageservingPublishSettings{#getimageservingpublishsettings}

僅供內部使用。 使用者應該參考影像伺服影像目錄參考 — 屬性參考區段。

语法

## 授權的使用者型別 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-79f0d54acd604ad2a5c96679334f2424}

**輸入(getImageServingPublishSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有影像伺服發佈設定的公司控制代碼。 |
| contextHandle | `xsd:string` | 是 | 處理發佈內容的動作。 |

**輸出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| publishSettingArray | `xsd:string` | 是 | 影像伺服器發佈設定的陣列。 |
