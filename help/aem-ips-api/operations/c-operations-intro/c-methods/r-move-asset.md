---
description: 将资产移动到特定文件夹。
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 17%

---

# moveAsset{#moveasset}

将资产移动到特定文件夹。

语法

## 授权用户类型 {#section-e4f2d2a58132450aa36da6377134211e}

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
| companyHandle | `xsd:string` | 是 | 对公司负责。 |
| assetHandle | `xsd:string` | 是 | 处理要移动的资产。 |
| folderHandle | `xsd:string` | 是 | 处理到目标文件夹。 |

**输出(moveAssetReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此代码示例可将资产移到文件夹。

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
