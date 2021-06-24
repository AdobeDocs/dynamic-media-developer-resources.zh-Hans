---
description: 设置ICC配置文件元数据字段。
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 14%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

设置ICC配置文件元数据字段。

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
| `*`companyHandle`*` | `xsd:string` | 是 | 对包含ICC配置文件的公司的句柄。 |
| `*`更新阵列`*` | `xsd:string` | 是 | ICC配置文件更新数组。 |

**输出(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功设置ICC配置文件字段的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试设置ICC配置文件字段时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试设置ICC配置文件字段时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试应用更新时，资产会生成警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与在操作尝试应用更新时生成错误的资产关联的详细信息数组。 |

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
