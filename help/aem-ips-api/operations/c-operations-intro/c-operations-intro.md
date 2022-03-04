---
description: 描述由IPS Web服务API处理的常见操作参数。
solution: Experience Manager
title: 操作方法
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 操作方法{#operations-methods}

本节介绍IPS Web服务API处理的常见操作参数。

有关每个操作参数的完整说明，请参阅 [操作参数](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## 句柄：关于 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

处理由某些API操作返回的引用IPS对象。 您还可以将句柄作为参数传递给后续操作调用。 句柄是字符串数据类型( `xsd:string`)。

句柄仅用于在单个应用程序会话期间使用。 此外，您应使句柄保持不变，因为它们的格式在IPS版本之间可能会发生更改。 在编写交互式应用程序时，您会实施会话超时并放弃会话之间的所有句柄，尤其是在IPS升级后。 在编写非交互式应用程序时，调用相应的操作以在每次运行应用程序时检索句柄。 以下Java/Axis2代码示例显示代码执行不正确且正确：

**句柄代码不正确**

此代码示例不正确，因为它包含公司句柄的硬编码值(555)。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正确的句柄代码**

此代码示例正确，因为它调用 `getCompanyInfo` 返回有效句柄。 它不依赖硬编码值。 使用此方法或其他等效的IPS API返回所需的句柄。

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 常见句柄类型 {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

大多数操作都要求您通过传入 `companyHandle` 参数。 公司句柄是某些操作(如 `getCompanyInfo`, `addCompany`和 `getCompanyMembership`.

**userHandle**

的 `userHandle` 参数是用于定位特定用户的操作的可选参数。 默认情况下，这些操作会以调用用户（其凭据被传入以进行身份验证的用户）为目标。 但是，具有适当权限的管理员用户可以指定其他用户。 例如， `setPassword` 操作通常会设置经过身份验证的用户的密码，但管理员可以使用 `userHandle` 参数来设置其他用户的密码。

对于需要公司上下文的操作(使用 `companyHandle` 参数)，则经过身份验证的用户和目标用户都必须是指定公司的成员。 对于不需要公司上下文的操作，经过身份验证的用户和目标用户都必须至少是一个共同公司的成员。

以下操作可以检索用户句柄：

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle和accessGroupHandle**

默认情况下，需要访问权限（读、写、删除）的操作在调用用户的权限上下文中运行。 某些操作允许您使用 `accessUserHandle` 或 `accessGroupHandle` 参数。 的 `accessUserHandle` 参数允许管理员模拟其他用户。 的 `accessGroupHandle` 参数允许调用者在特定用户组的上下文中操作。

**responseFieldArray和excludeFieldArray**

某些操作允许调用方限制响应中包含哪些字段。 限制字段有助于减少处理请求所需的时间和内存，并减小响应数据的大小。 调用方可通过传递 `responseFieldArray` 参数，或通过枚举来列出排除的字段 `excludeFieldArray` 参数。

两者兼有 `responseFieldArray` 和 `excludeFieldArray` 使用以 `/`. 例如，指定 `searchAssets` 仅返回每个资产的名称、上次修改日期和元数据，请参阅以下内容：

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同样，要返回所有字段（权限除外）：

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

请注意，节点路径是相对于返回节点根的。 如果您指定的是一个复杂类型字段，而没有任何子元素(例如， `assetArray/items/imageInfo`)，则会包含其所有子元素。 如果在复杂类型字段中指定一个或多个子元素(例如， `assetArray/items/imageInfo/originalPath`)，则只包含这些子元素。

如果不包含 `responseFieldArray` 或 `excludeFieldArray` 在请求中，将返回所有字段。

**区域设置**

自IPS 4.0起，IPS API通过传递 `authHeader` 区域设置参数。 如果区域设置参数不存在，则HTTP标头 `Accept-Language` 中，将使用。 如果此标头不存在，则使用IPS服务器的默认区域设置。

某些操作还采用显式区域设置参数，这些参数可能与操作区域设置上下文不同。 例如， `submitJob` 操作需要 `locale` 参数，用于设置用于作业日志记录和电子邮件通知的区域设置。

区域设置参数使用格式 `<language_code>[-<country_code>]`

其中，语言代码是ISO-639指定的小写字母双字母代码，而可选国家/地区代码是ISO-3266指定的大写双字母代码。 例如，美式英语的区域设置字符串为 `en-US`.
