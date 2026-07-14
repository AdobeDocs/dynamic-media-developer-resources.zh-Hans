---
description: 返回资产的发布历史记录。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 15%

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
| companyHandle | `xsd:string` | 是 | 具有资产发布历史记录的公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 包含要检查的发布历史记录的资源。 |

**输出(getAssetPublishHistoryReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | 是 | 资源的发布历史记录。 |

## 示例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

此代码示例返回资源的发布历史记录。 如果服务器返回空数组，则表示从未发布资产。

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

