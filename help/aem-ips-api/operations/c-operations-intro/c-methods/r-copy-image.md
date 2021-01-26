---
description: 创建现有图像资产的副本。 将应用指定的图像服务器协议命令生成新副本
seo-description: 创建现有图像资产的副本。 将应用指定的图像服务器协议命令生成新副本
seo-title: copyImage
solution: Experience Manager
title: copyImage
topic: Dynamic Media Image Production System API
uuid: ae24f0cc-bcf0-4652-a67d-ed69f8a0da92
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 19%

---


# copyImage{#copyimage}

创建现有图像资产的副本。 将应用指定的图像服务器协议命令生成新副本

语法

## 授权用户类型{#section-c9fe7abb550e495f832234f845db7d6e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-bf36fcbfda6742f5b9c6b02ea27e5b9d}

**输入(copyImageParam)**

<table id="table_F6B14D4875F2424D98B8C4899B1DD867"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>包含图像的公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>图像资产的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> folderHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要复制图像的文件夹的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 名称</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>新图像的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> urlModifier</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(copyImageParam)**

<table id="table_5E4ED83047314DFABC1BFAAC76C0EAC3"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>复制图像的手柄。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-c30a4017001146e7befbbfc5ffcb7593}

示例代码复制由公司、资产、文件夹句柄和名称指定的图像。

**请求**

```java
<copyImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>Copy_macbookwin1</name>
   <urlModifier/>
</copyImageParam>
```

**响应**

```java
<copyImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|943|1|580</assetHandle>
</copyImageReturn>
```

