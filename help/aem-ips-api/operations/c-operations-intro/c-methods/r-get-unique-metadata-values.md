---
description: 获取唯一元数据字段值。
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 24%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

获取唯一元数据字段值。

语法

## 授权用户类型{#section-6a6b67e10a4c4e7bb18306115713380e}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`fieldHandle`*` | `xsd:string` | 否 | 处理元数据字段。 |

**输出(getUniqueMetadataValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`values`*` | `type:StringArray` |  |  |

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

