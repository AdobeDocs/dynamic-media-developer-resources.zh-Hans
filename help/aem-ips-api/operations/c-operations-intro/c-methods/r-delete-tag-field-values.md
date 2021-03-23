---
description: 从标记字段的字典中删除标记字段值。
seo-description: 从标记字段的字典中删除标记字段值。
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 11%

---


# deleteTagFieldValues{#deletetagfieldvalues}

从标记字段的字典中删除标记字段值。

## 授权用户类型{#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5db64a6ae238426395bc760b83587260}

**输入(deleteTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含标签字段的公司的句柄。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 要修改的标记字段的句柄。 |
| `*`valueArray`*` | `types:StringArray` | 是 | 要从字段的词典中删除的标记值数组。 |

**输出(deleteTagFieldValuesParam)**

IPS API不返回此操作的响应。

## 示例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**请求**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**响应**

无。
