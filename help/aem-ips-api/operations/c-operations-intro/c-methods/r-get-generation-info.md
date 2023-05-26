---
description: 根据传入的参数返回2种不同类型的信息。 originatorHandle返回有关从指定资源生成的资源的信息。 generateHandle返回有关用于生成指定资源或文件的步骤的信息。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 10%

---

# getGenerationInfo{#getgenerationinfo}

根据传入的参数返回2种不同类型的信息。 originatorHandle返回有关从指定资源生成的资源的信息。 generateHandle返回有关用于生成指定资源或文件的步骤的信息。

语法

## 授权用户类型 {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-b7fa94c82147455888e8469fa5f6922b}

**输入(getGenerationInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 代码短语 | `xsd:string` | 是 | 公司的把手。 |
| 代码短语 | `xsd:string` | 否 | 生成时使用的引擎。 请参阅字体样式。 |
| 代码短语 | `xsd:string` | 否 | 要查询生成的资产的资产的资产句柄。 |
| 代码短语 | `xsd:string` | 否 | 要查询其生成中使用的资源和引擎的资源句柄。 |
| 代码短语 | `xsd:StringArray` | 否 | 操作中包含的属性。 |
| 代码短语 | `xsd:StringArray` | 否 | 从操作中排除的属性。 |

**输出(getGenerationInfoReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | 是 | 层代信息数组。 |

## 示例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此代码示例返回有关从特定资源生成的资源的信息。 它不会检索有关用于生成指定资产的步骤的信息。 为简短起见，响应将被截断。

**请求**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**响应**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
