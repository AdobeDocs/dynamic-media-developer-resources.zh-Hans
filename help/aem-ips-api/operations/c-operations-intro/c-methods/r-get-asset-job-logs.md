---
description: 取得資產的工作記錄檔。 陣列中傳回的專案包含該資產之作業記錄中每個專案的詳細資訊。 logMessage回應欄位已根據authHeader欄位進行本地化。
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---

# getAssetJobLogs{#getassetjoblogs}

取得資產的工作記錄檔。 陣列中傳回的專案包含該資產之作業記錄中每個專案的詳細資訊。 logMessage回應欄位已根據authHeader欄位進行本地化。

语法

## 授權的使用者型別 {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-9586617e124b4da4acb6b66b2a9adad8}

**輸入(getAssetJobLogsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資產所屬公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 包含要擷取之工作記錄檔的資產的控點。 |

**輸出(getAssetJobLogsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobLogArray | `types:AssetJobLogArray` | 是 | 工作記錄陣列。 |

## 示例 {#section-f03d7f3ec5d043d38227f926fb7609f6}

此程式碼範例會擷取特定資產的工作記錄。 回應會傳回工作記錄陣列，內含使用資產之所有工作的詳細資訊。

**请求**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**响应**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
