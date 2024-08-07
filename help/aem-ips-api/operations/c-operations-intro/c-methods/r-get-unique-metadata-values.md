---
description: 获取唯一的元数据字段值。
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 24%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

获取唯一的元数据字段值。

语法

## 授权用户类型 {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-b9d1413811c24566b6d095701f0f66db}

**输入(getUniqueMetadataValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 处理公司。 |
| fieldHandle | `xsd:string` | 否 | 元数据字段的句柄。 |

**输出(getUniqueMetadataValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 值 | `type:StringArray` |  |  |

## 示例 {#section-440f3bc3e5be436cb6ec26117d05f476}

此代码示例使用字段句柄返回特定的元数据值。

**请求**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**响应**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```
