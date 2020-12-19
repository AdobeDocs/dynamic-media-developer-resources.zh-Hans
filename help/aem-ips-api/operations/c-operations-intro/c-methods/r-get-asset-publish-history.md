---
description: 返回资产的发布历史记录。
seo-description: 返回资产的发布历史记录。
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
topic: Scene7 Image Production System API
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---


# getAssetPublishHistory{#getassetpublishhistory}

返回资产的发布历史记录。

语法

## 授权用户类型{#section-3b9d6a129093458fa8890139a2718912}

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 具有资产发布历史记录的公司的句柄。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 包含要检查的发布历史记录的资产。 |

**输出(getAssetPublishHistoryReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`pubHistoryArray`*` | `types:PublishHistoryArray` | 是 | 资产的发布历史记录。 |

## 示例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

此代码示例返回资产的发布历史记录。 如果服务器返回空数组，则资产从未发布过。

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

