---
description: 获取特定字段中使用的字符列表。
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
TQID: 'https://experienceleague.adobe.com/ojFrVXletWbKwGTjfJIfRI9M9BBJT7zj4AGrvVMP6T8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 10%

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
| charField | `xsd:string` | 是 | 确定要搜索的垃圾桶状态。 |
| includeInactive | `xsd:boolean` | 是 | 包含或排除不活动的用户。 非IPS管理员用户必须是至少一个公司的活跃成员，才能获得发出任何API调用的授权。 如果用户没有活动的公司成员资格，则会返回授权错误。 |
| includInvalid | `xsd:boolean` | 否 | 包含或排除无效用户。 |
| companyHandleArray | `types:HandleArray` | 否 | 根据公司筛选结果。 |
| groupHandleArray | `types:HandleArray` | 否 | 根据组筛选结果。 |
| userRoleArray | `types:StringArray` | 否 | 根据用户角色筛选结果。 |
| numChars | `xsd:int` | 否 | 启用>1个字符。 |

**输出(getUserCharsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userCharsArray | `types:StringArray` | 是 | 字符前缀的数组。 |

## 示例 {#section-3702f165e8b041139a6144f4a76ca25f}

此代码示例返回：

* 特定公司用户的姓氏的第一个字符。
* 一组组。
* 一组用户角色。

“用户字符过滤字段”字符串常量确定返回的用户字符类型。

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

