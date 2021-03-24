---
description: 设置资产的元数据值。 使用一组元数据更新在批处理中设置值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic，SDK/API，元数据，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

设置资产的元数据值。 使用一组元数据更新在批处理中设置值。

语法

## 授权用户类型{#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对资产的读取权限。

## 参数 {#section-bcdcff30905e444388811e897b2824bd}

**输入(setAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要更新的资产的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 资产的句柄。 |
| `*`updateArray`*` | `types:MetadataUpdateArray` | 是 | 元数据更新数组中的更新。 |

**输出(setAssetMetadataReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此代码示例使用一组元数据更新来设置指定资产的元数据。

**请求**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**响应**

无。
