---
description: 获取数组中的所有用户。
solution: Experience Manager
title: getAllUsers
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 22%

---


# getAllUsers{#getallusers}

获取数组中的所有用户。

语法

## 授权用户类型{#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-f092ca72f2024d66a1cec690aeab870a}

**输入(getAllUsersParam)**

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">设置为： 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108"><span class="codeph"> trueto包</span> 括无效用户。 </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> </span> false不能忽略无效用户。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**输出(getAllUsersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | 是 | 所有用户的数组。 |
| `*`代码短语`*` | `Code Phrase` |  |  |

## 示例 {#section-9c9a2d335513478da20652c1b1443731}

此代码示例返回所有用户。 响应被截断以便简短。

**请求**

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**响应**

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```

