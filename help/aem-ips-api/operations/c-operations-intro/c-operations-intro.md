---
description: 本节介绍由IPS Web服务API处理的常见操作参数。
seo-description: 本节介绍由IPS Web服务API处理的常见操作参数。
seo-title: 操作方法
solution: Experience Manager
title: 操作方法
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# 操作方法{#operations-methods}

本节介绍由IPS Web服务API处理的常见操作参数。

有关每个操作参数的完整说明，请参阅操 [作参数](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)。

## 句柄：关于 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

处理由某些API操作返回的引用IPS对象。 您还可以将句柄作为参数传递给后续操作调用。 句柄是字符串数据类型( `xsd:string`)。

句柄仅用于单个应用程序会话期间。 此外，您应该使句柄保持不变，因为它们的格式可以在IPS版本之间更改。 在编写交互式应用程序时，您将实现会话超时并放弃会话之间的所有句柄，尤其是在IPS升级后。 在编写非交互式应用程序时，每次运行应用程序时调用相应的操作以检索处理程序。 以下Java/Axis2代码示例显示代码执行错误和正确：

**处理代码不正确**

此代码范例不正确，因为它包含用于公司句柄的硬编码值(555)。

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**正确的处理代码**

此代码示例正确，因为它调用 `getCompanyInfo` 返回有效句柄。 它不依赖于硬编码值。 使用此方法（或其他等效的IPS API）返回所需的句柄。

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

大多数操作都要求您通过传入参数来设置公司上 `companyHandle` 下文。 公司手柄是某些操作（如、和）返回 `getCompanyInfo`的 `addCompany`指针 `getCompanyMembership`。

**userHandle**

该参 `userHandle` 数是目标特定用户的操作的可选参数。 默认情况下，这些操作将目标主叫用户（其凭据已传入以进行身份验证的用户）。 但是，具有相应权限的管理员用户可以指定其他用户。 例如，该操 `setPassword` 作通常设置已验证用户的口令，但管理员可以使用该参数为其 `userHandle` 他用户设置口令。

对于需要公司上下文(使用参 `companyHandle` 数)的操作，已验证和目标用户都必须是指定公司的成员。 对于不需要公司上下文的操作，已验证的用户和目标用户都必须是至少一个共同公司的成员。

以下操作可以检索用户句柄：

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle和accessGroupHandle**

默认情况下，需要访问权限（读、写、删除）的操作在调用用户的权限上下文中进行。 某些操作允许您使用或参数修改此 `accessUserHandle` 上下 `accessGroupHandle` 文。 该参 `accessUserHandle` 数允许管理员模拟其他用户。 该参 `accessGroupHandle` 数允许调用者在特定用户组的上下文中操作。

**responseFieldArray和excludeFieldArray**

某些操作允许调用者限制响应中包含的字段。 限制字段有助于减少处理请求所需的时间和内存并减小响应数据的大小。 调用者可以通过传递参数来请求特定的字段列表, `responseFieldArray` 或者通过该参数通过枚举的被排除字段列表来请求特定的 `excludeFieldArray` 字段。

使用 `responseFieldArray` 以 `excludeFieldArray` 分隔的节点路径指定字段和字段 `/`。 例如，要指定仅返回每 `searchAssets` 个资产的名称、上次修改日期和元数据，请参阅以下内容：

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

同样，要返回所有字段（权限除外）:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

请注意，节点路径是相对于返回节点根的。 如果指定一个不带任何子元素(例如， `assetArray/items/imageInfo`)的复杂类型字段，则其所有子元素都将包含在内。 如果在复杂类型字段(例如， `assetArray/items/imageInfo/originalPath`)中指定一个或多个子元素，则只包括这些子元素。

如果请求中不包 `responseFieldArray` 含或 `excludeFieldArray` 不包含，则返回所有字段。

**区域设置**

自IPS 4.0以来，IPS API通过传递区域设置参数支持设置操作的区域设 `authHeader` 置上下文。 如果区域设置参数不存在，则将使 `Accept-Language` 用HTTP头。 如果此头也不存在，则将使用IPS服务器的默认区域设置。

某些操作还采用显式区域设置参数，这可能与操作区域设置上下文不同。 例如，该操作会 `submitJob` 使用一个参 `locale` 数来设置用于作业记录和电子邮件通知的区域设置。

区域设置参数使用格式 `<language_code>[-<country_code>]`

如果语言代码是ISO-639指定的小写双字母代码，而可选国家／地区代码是ISO-3266指定的大写双字母代码。 例如，“美国英语”的区域设置字符串为 `en-US`。
