---
description: 设置字体元数据字段。
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
TQID: 'https://experienceleague.adobe.com/IkKqBLa2j-YKPTp5Nsttxb8GgpPgcSee1zG0asjxNyQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 13%

---

# batchSetFontFields{#batchsetfontfields}

设置字体元数据字段。

## 授权用户类型 {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-836f5948d00a46e98ccb62f0573e4e68}

**输入(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 处理包含字体的公司。 |
| updateArray | `types:FontFieldUpdateArray` | 是 | 字体字段更新的数组。 |

**输出(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功设置的字体字段数。 |
| warningcount | `xsd:int` | 是 | 操作尝试设置字体字段时生成的警告数。 |
| errorCount | `xsd:int` | 是 | 操作尝试设置字体字段时生成的错误数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，在操作尝试应用更新时这些资产会生成警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试应用更新时这些资产会生成错误。 |

## 示例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**请求**

```javascript {.line-numbers}
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

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

