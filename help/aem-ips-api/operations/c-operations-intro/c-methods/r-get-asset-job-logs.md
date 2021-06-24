---
description: 获取资产的作业日志。 数组中返回的项目包含有关该资产作业日志中每个条目的详细信息。 logMessage响应字段基于authHeader字段进行本地化。
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 9%

---

# getAssetJobLogs{#getassetjoblogs}

获取资产的作业日志。 数组中返回的项目包含有关该资产作业日志中每个条目的详细信息。 logMessage响应字段基于authHeader字段进行本地化。

语法

## 授权用户类型 {#section-72b98cdb0f6f47f5aabdc183a45ea577}

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

**输入(getAssetJobLogsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 资产所属公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要检索作业日志的资产句柄。 |

**Output(getAssetJobLogsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | 是 | 作业日志阵列。 |

## 示例 {#section-f03d7f3ec5d043d38227f926fb7609f6}

此代码示例可检索特定资产的作业日志。 该响应会返回一个作业日志数组，其中包含有关使用该资产的所有作业的详细信息。

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
