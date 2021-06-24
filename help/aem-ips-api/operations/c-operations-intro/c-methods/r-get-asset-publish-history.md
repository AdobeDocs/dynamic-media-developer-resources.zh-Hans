---
description: 返回资产的发布历史记录。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 16%

---

# getAssetPublishHistory{#getassetpublishhistory}

返回资产的发布历史记录。

语法

## 授权用户类型 {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-3541bd9914a44b89acfc1d419b560ee6}

**输入(getAssetPublishHistoryParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 具有资产发布历史记录的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 包含要检查的发布历史记录的资产。 |

**输出(getAssetPublishHistoryReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | 是 | 资产的发布历史记录。 |

## 示例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

此代码示例可返回资产的发布历史记录。 如果服务器返回空数组，则资产从未发布。

**请求**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**响应**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
