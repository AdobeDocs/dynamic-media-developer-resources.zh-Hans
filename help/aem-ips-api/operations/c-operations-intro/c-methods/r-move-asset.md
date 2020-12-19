---
description: 将资产移至特定文件夹。
seo-description: 将资产移至特定文件夹。
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 15%

---


# moveAsset{#moveasset}

将资产移至特定文件夹。

语法

## 授权用户类型{#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-dd0bbdf293aa4563af70a91f97c861f1}

**输入(moveAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| ` *`assetHandle`*` | `xsd:string` | 是 | 处理要移动的资产。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 处理目标文件夹。 |

**输出(moveAssetReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此代码示例将资产移动到文件夹。

**请求**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**响应**

无。
