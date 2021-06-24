---
description: 根据传入的参数返回2种不同类型的信息。 originatorHandle返回有关从指定资产生成的资产的信息。 generateHandle返回有关用于生成指定资产或文件的步骤的信息。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

根据传入的参数返回2种不同类型的信息。 originatorHandle返回有关从指定资产生成的资产的信息。 generateHandle返回有关用于生成指定资产或文件的步骤的信息。

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
| `*`代码短语`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`代码短语`*` | `xsd:string` | 否 | 一代中使用的引擎。 请参阅字体样式。 |
| `*`代码短语`*` | `xsd:string` | 否 | 要查询已生成资产的资产的句柄。 |
| `*`代码短语`*` | `xsd:string` | 否 | 用于查询在生成资产时使用的资产和引擎的资产句柄。 |
| `*`代码短语`*` | `xsd:StringArray` | 否 | 操作中包含的属性。 |
| `*`代码短语`*` | `xsd:StringArray` | 否 | 从操作中排除的属性。 |

**输出(getGenerationInfoReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | 是 | 生成信息的数组。 |

## 示例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此代码示例可返回有关从特定资产生成的资产的信息。 它不会检索有关用于生成指定资产的步骤的信息。 响应因简短而被截断。

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
