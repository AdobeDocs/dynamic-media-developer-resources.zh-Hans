---
description: 获取有关资产的搜索字符串、关键字和其他信息。 响应包含有关资产的其他信息。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

获取有关资产的搜索字符串、关键字和其他信息。 响应包含有关资产的其他信息。

语法

## 授权用户类型 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-c1efda4bb15349a68b276bafee8c18fd}

**输入(getSearchStringsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理资产。 |

**Output(getSearchStringsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | 是 | 资产搜索字符串的数组。 |

## 示例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此代码示例可返回资产特定的搜索字符串。 响应返回一个空数组。

**请求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**响应**

无。
