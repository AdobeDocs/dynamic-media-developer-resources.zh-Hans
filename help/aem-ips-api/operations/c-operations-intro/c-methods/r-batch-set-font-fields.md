---
description: 设置字体元数据字段。
seo-description: 设置字体元数据字段。
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---


# batchSetFontFields{#batchsetfontfields}

设置字体元数据字段。

## 授权用户类型{#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对包含字体的公司进行处理。 |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | 是 | 字体字段更新的数组。 |

**输出(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功设置字体字段的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试设置字体字段时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试设置字体字段时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试应用更新时生成警告的与资产关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与在操作尝试应用更新时生成错误的资产关联的详细信息数组。 |

## 示例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**请求**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**响应**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

