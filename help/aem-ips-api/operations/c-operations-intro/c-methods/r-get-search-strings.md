---
description: 获取搜索字符串、关键字和有关资产的其他信息。 该响应包含有关资产的其他信息。
seo-description: 获取搜索字符串、关键字和有关资产的其他信息。 该响应包含有关资产的其他信息。
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Dynamic Media Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 14%

---


# getSearchStrings{#getsearchstrings}

获取搜索字符串、关键字和有关资产的其他信息。 该响应包含有关资产的其他信息。

语法

## 授权用户类型{#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-c1efda4bb15349a68b276bafee8c18fd}

**输入(getSearchStringsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理资产。 |

**输出(getSearchStringsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | 是 | 资产搜索字符串的数组。 |

## 示例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此代码示例返回资产特定搜索字符串。 响应返回空数组。

**请求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**响应**

无。
