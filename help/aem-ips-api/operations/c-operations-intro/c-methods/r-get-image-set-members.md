---
description: 取得影像集中的成員陣列。
solution: Experience Manager
title: getImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---

# getImageSetMember{#getimagesetmembers}

取得影像集中的成員陣列。

语法

## 授權的使用者型別 {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要影像和成員集資產的讀取存取權。

## 参数 {#section-a67ba98095574533980997c83ceaa316}

**輸入(getImageSetMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含影像集的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 影像集資產控制點。 |

**輸出(getImageSetMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | 否 | 影像整合員的陣列。 |

## 示例 {#section-888a9a78033346f39b171229de93dfa0}

此程式碼範例會傳回特定的影像整合員。 回應會傳回空白陣列。

**请求**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**响应**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
