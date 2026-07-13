---
description: 将新标记值添加到现有标记字段的词典。
solution: Experience Manager
title: addTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: 'https://experienceleague.adobe.com/-DA9IYswE5Mfflys-Cn0Gi62OsMU3O1QYIIKYJNq9QU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 12%

---

# addTagFieldValue{#addtagfieldvalues}

将新标记值添加到现有标记字段的词典。

语法

## 授权用户类型 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**输入(addTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含标记字段的公司句柄。 |
| fieldHandle | `xsd:string` | 是 | 要修改的标记字段的句柄。 |
| valueArray | `xsd:string` | 是 | 要添加到字段现有字典的标记值数组。 |

**输出(addTagFieldValuesParam)**

IPS API不返回此操作的响应。

## 示例 {#section-c4049392f1c548f883b8b1f8f167bada}

**请求**

```java {.line-numbers}
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**响应**

无。

