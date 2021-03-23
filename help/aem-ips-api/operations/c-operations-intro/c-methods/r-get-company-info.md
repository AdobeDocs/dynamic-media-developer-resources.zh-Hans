---
description: 返回有关指定公司的信息，包括公司句柄、公司名称、根路径和过期日期。 必须指定要检索其信息的companyHandle或companyName。
seo-description: 返回有关指定公司的信息，包括公司句柄、公司名称、根路径和过期日期。 必须指定要检索其信息的companyHandle或companyName。
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 8%

---


# getCompanyInfo{#getcompanyinfo}

返回有关指定公司的信息，包括公司句柄、公司名称、根路径和过期日期。 必须指定要检索其信息的companyHandle或companyName。

语法

## 授权用户类型{#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7dec8871c89a414c9f066adade1831d8}

**输入(getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span>或<span class="codeph"> <span class="varname"> companyName</span> </span>为必需项。 </p> </td> 
   <td colname="col4"> <p>要获取其信息的公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span>或<span class="codeph"> <span class="varname"> companyName</span> </span>为必需项。 </p> </td> 
   <td colname="col4"> <p>要获取其信息的公司的名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：公司</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>处理和有关公司的其他描述性信息。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

此代码示例使用公司名和句柄返回有关公司的所有信息。 它返回与创建公司时收到的响应类似的数据。

**请求**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**响应**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

