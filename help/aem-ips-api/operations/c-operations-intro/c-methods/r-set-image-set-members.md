---
description: 设置与图像集关联的资产的列表。
seo-description: 设置与图像集关联的资产的列表。
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 11%

---


# setImageSetMembers{#setimagesetmembers}

设置与图像集关联的资产的列表。

此操作会忽略`ImageSets`和`SpinSets`的`pageReset`参数，并将值强制为true。

## 授权用户类型{#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对图像集资产的读和写访问权限，并且对每个成员资产具有读访问权限。

## 参数 {#section-2f46efcd24c648aeacba738509426e46}

**Input(setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>公司手柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像集手柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 属于图像集的资产成员的数组。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(setImageSetMembersReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-7b87219034464aa98524178ccee27738}

此代码示例使用成员数组设置图像集的成员。

**请求**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**响应**

无。
