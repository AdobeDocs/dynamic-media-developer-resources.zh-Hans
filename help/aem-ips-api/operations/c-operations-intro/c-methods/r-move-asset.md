---
description: 将资产移至特定文件夹。
seo-description: 将资产移至特定文件夹。
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 13%

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
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理要移动的资产。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 处理目标文件夹。 |

**输出(moveAssetReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此代码示例将资产移到文件夹。

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
