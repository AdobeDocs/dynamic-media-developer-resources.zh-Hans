---
description: 刪除資產。
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 13%

---

# deleteAsset{#deleteasset}

刪除資產。

语法

## 授權的使用者型別 {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和刪除存取權。

## 参数 {#section-0eed164e278b456fbdfb7a50727a0416}

**輸入(deleteAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 資料夾所屬公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 要刪除之資產的控點。 |

**輸出(deleteAssetParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-d5657289f5234bb0a613dcf691507958}

此範常式式碼會從特定公司刪除任何型別的資產。 它需要資產控制代碼，您必須從其他作業取得。

**请求**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**响应**

无。
