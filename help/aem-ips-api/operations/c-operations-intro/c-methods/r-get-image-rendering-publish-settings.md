---
description: 僅供內部使用。 請參閱影像演算材質目錄參考目錄屬性區段。
solution: Experience Manager
title: getimagerenderingpublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

---

# getimagerenderingpublishSettings{#getimagerenderingpublishsettings}

僅供內部使用。 請參閱影像演算材質目錄參考目錄屬性區段。

语法

## 授權的使用者型別 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-4f2cb8c589384816bb2525654ec49963}

**輸入(getImageRenderingPublishSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您要取得其影像演算發佈設定的公司控制代碼。 |
| contextHandle | `xsd:string` | 是 | 處理發佈內容的動作。 |

**輸出(getImageRenderingPublishSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | 是 | 影像演算發佈設定。 |
