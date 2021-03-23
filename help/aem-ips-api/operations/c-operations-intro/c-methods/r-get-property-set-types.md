---
description: 获取与指定公司关联的属性集类型，或者如果未指定公司，则获取全局属性集类型。
seo-description: 获取与指定公司关联的属性集类型，或者如果未指定公司，则获取全局属性集类型。
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 12%

---


# getPropertySetTypes{#getpropertysettypes}

获取与指定公司关联的属性集类型，或者如果未指定公司，则获取全局属性集类型。

语法

## 授权用户类型{#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input(getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">属性集类型所关联的公司的句柄。 <p>如果要返回全局属性集类型，则省略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(getPropertySetTypesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | 是 | 与指定公司关联的属性集类型的数组，或者如果未指定公司，则全局属性集类型。 |

## 示例 {#section-280c406a90864409856aee44d4069a52}

**请求**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**响应**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

