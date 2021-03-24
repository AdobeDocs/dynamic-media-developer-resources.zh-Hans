---
description: 获取图像集中的成员数组。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

获取图像集中的成员数组。

语法

## 授权用户类型{#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>需要对图像和成员集资产的读取访问权限。

## 参数 {#section-a67ba98095574533980997c83ceaa316}

**输入(getImageSetMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含图像集的公司的手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 图像集资产句柄。 |

**输出(getImageSetMembersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | 否 | 图像集成员的数组。 |

## 示例 {#section-888a9a78033346f39b171229de93dfa0}

此代码示例返回特定图像集成员。 响应返回空数组。

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

