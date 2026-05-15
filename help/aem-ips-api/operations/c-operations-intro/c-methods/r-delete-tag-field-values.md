---
description: 从标记字段的词典中删除标记字段值。
solution: Experience Manager
title: deleteTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 11%

---

# deleteTagFieldValue{#deletetagfieldvalues}

从标记字段的词典中删除标记字段值。

## 授权用户类型 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5db64a6ae238426395bc760b83587260}

**输入(deleteTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含标记字段的公司句柄。 |
| fieldHandle | `xsd:string` | 是 | 要修改的标记字段的句柄。 |
| valueArray | `types:StringArray` | 是 | 要从字段字典中删除的标记值数组。 |

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
