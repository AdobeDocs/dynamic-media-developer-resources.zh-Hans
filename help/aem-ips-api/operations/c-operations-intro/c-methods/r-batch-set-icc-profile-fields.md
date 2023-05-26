---
description: 设置ICC配置文件元数据字段。
solution: Experience Manager
title: batchsetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 14%

---

# batchsetIccProfileFields{#batchseticcprofilefields}

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
| companyHandle | `xsd:string` | 是 | 包含ICC配置文件的公司的句柄。 |
| 更新数组 | `xsd:string` | 是 | ICC配置文件更新的数组。 |

**输出(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功设置的ICC配置文件字段数。 |
| warningCount | `xsd:int` | 是 | 当操作尝试设置ICC配置文件字段时生成的警告数。 |
| 错误计数 | `xsd:int` | 是 | 操作尝试设置ICC配置文件字段时生成的错误数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 与资源关联的详细信息数组，在操作尝试应用更新时这些资源会生成警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，在操作尝试应用更新时这些资产会生成错误。 |

## 示例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**请求**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
