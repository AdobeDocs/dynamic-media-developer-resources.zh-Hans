---
description: 使用公司句柄获取资产集类型和资产集类型的名称。 它将获得一个类型结构，该结构具有类型和属性类型的句柄。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 10%

---

# getPropertySetType{#getpropertysettype}

使用公司句柄获取资产集类型和资产集类型的名称。 它将获得一个类型结构，该结构具有类型和属性类型的句柄。

语法

## 授权用户类型 {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-c9a53400c44744668bd7915f72d2bf3d}

**输入(getPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的把手。 可选，因为资产集类型可以属于多个公司。 |
| `*`name`*` | `xsd:string` | 是 | 属性集类型名称。 |

**Output(getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">包含以下项的类型结构： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">把手。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">类型名称。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">属性类型。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">指示类型是否允许多个属性类型的值。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-1b57199415e34a8fa449f864f8895b14}

此代码示例按名称返回属性集类型。

**请求**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**响应**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```
