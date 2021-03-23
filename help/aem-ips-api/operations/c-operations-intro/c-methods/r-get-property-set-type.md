---
description: 使用公司句柄和属性集类型的名称获取属性集类型。 它获取一个类型结构，该结构具有类型和属性类型的句柄。
seo-description: 使用公司句柄和属性集类型的名称获取属性集类型。 它获取一个类型结构，该结构具有类型和属性类型的句柄。
seo-title: getPropertySetType
solution: Experience Manager
title: getPropertySetType
uuid: 203fa949-a81e-455a-a83e-576b6f65e3af
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 8%

---


# getPropertySetType{#getpropertysettype}

使用公司句柄和属性集类型的名称获取属性集类型。 它获取一个类型结构，该结构具有类型和属性类型的句柄。

语法

## 授权用户类型{#section-2b291d32f95b4a3d854429124cbae24c}

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

**Input(getPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的手柄。 可选，因为属性集类型可以属于多个公司。 |
| `*`name`*` | `xsd:string` | 是 | 属性集类型名称。 |

**输出(getPropertySetTypeReturn)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 类型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">包含以下项的类型结构： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">处理。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">键入名称。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">属性类型。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">指示类型是否允许多个属性类型的值。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-1b57199415e34a8fa449f864f8895b14}

此代码示例返回按名称设置类型的属性。

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

