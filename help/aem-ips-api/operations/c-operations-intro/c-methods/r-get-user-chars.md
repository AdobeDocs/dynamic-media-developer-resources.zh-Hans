---
description: 获取特定字段中使用的字符列表。
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 11%

---

# getUserChars{#getuserchars}

获取特定字段中使用的字符列表。

语法

## 授权用户类型 {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-93107d87f1b24fc8ad276dfee5e30b63}

**输入(getUserCharsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | 是 | 确定要搜索的垃圾桶状态。 |
| `*`includeInactive`*` | `xsd:boolean` | 是 | 包括或排除不活动的用户。 非IPS管理员用户必须是至少一家公司的活动成员，才能获得授权进行任何API调用。 如果用户没有有效的公司成员资格，则会返回授权错误。 |
| `*`includeInvalid`*` | `xsd:boolean` | 否 | 包括或排除无效用户。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 否 | 根据公司筛选结果。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 否 | 根据组筛选结果。 |
| `*`userRoleArray`*` | `types:StringArray` | 否 | 根据用户角色筛选结果。 |
| `*`numChars`*` | `xsd:int` | 否 | 启用超过1个字符。 |

**Output(getUserCharsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | 是 | 字符前缀数组。 |

## 示例 {#section-3702f165e8b041139a6144f4a76ca25f}

此代码示例会返回：

* 特定公司用户姓氏的首字母。
* 一组组。
* 一组用户角色。

用户字符过滤器字段字符串常量确定返回的用户字符类型。

**请求**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**响应**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
