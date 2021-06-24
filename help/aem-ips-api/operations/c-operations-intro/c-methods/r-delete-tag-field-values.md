---
description: 从标记字段的字典中删除标记字段值。
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 13%

---

# deleteTagFieldValues{#deletetagfieldvalues}

从标记字段的字典中删除标记字段值。

## 授权用户类型 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5db64a6ae238426395bc760b83587260}

**Input(deleteTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含标记字段的公司的句柄。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 要修改的标记字段的句柄。 |
| `*`valueArray`*` | `types:StringArray` | 是 | 要从字段词典中删除的标记值数组。 |

**输出(deleteTagFieldValuesParam)**

IPS API不会返回此操作的响应。

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
