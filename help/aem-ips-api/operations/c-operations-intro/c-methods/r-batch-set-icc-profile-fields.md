---
description: 设置ICC用户档案元数据字段。
seo-description: 设置ICC用户档案元数据字段。
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetIccProfileFields{#batchseticcprofilefields}

设置ICC用户档案元数据字段。

语法

## 授权用户类型 {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**输入(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 对包含ICC公司的用户档案进行处理。 |
| ` *`更新阵列`*` | `xsd:string` | 是 | ICC用户档案更新阵列。 |

**输出(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 是 | 成功设置ICC用户档案字段的数量。 |
| ` *`warningCount`*` | `xsd:int` | 是 | 尝试设置ICC用户档案字段时生成的警告数。 |
| ` *`errorCount`*` | `xsd:int` | 是 | 尝试设置ICC用户档案字段时生成的错误数。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试应用更新时，这些资产生成了警告。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试应用更新时生成错误的与资产关联的详细信息数组。 |

## 示例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**请求**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**响应**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

