---
description: 获取图像集中的成员数组。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 14%

---

# getImageSetMembers{#getimagesetmembers}

获取图像集中的成员数组。

语法

## 授权用户类型 {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>需要拥有对图像和成员集资源的读取权限。

## 参数 {#section-a67ba98095574533980997c83ceaa316}

**输入(getImageSetMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含图像集的公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 图像集资源句柄。 |

**输出(getImageSetMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | 否 | 图像集成员的数组。 |

## 示例 {#section-888a9a78033346f39b171229de93dfa0}

此代码示例返回特定的图像集成员。 响应返回空数组。

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
