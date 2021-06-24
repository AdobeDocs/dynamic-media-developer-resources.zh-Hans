---
description: 创建新图像映射或编辑现有映射。
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 15%

---

# saveImageMap{#saveimagemap}

创建新图像映射或编辑现有映射。

语法

## 授权用户类型 {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读取和写入权限。

## 参数 {#section-64f7f5fd8f954fba9fa30eeee556863a}

**输入(saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含要保存的图像映射的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射所属的图像资产的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 图像映射的句柄。 如果为NULL，则创建图像映射。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 创建或保存的图像映射的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 选择区域形状。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 地区  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 以逗号分隔的点列表，用于定义区域。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 操作  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>与IPS接口中指定的图像映射关联的<span class="codeph"> href </span>值。 </p> <p>要获取<span class="codeph"> href </span>值，请单击IPS界面中的图像，将URL复制并粘贴到此元素中，然后将IPS URL格式化为正确的URL。 例如， <span class="codeph">和</span>将变为<span class="codeph"> &amp;amp;</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 位置  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射列表中的顺序（Z轴）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 已启用  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**输出(saveImageMapReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 是 | 新图像映射或编辑图像映射的句柄。 |

## 示例 {#section-fdac488b640f427c8aa3d549c5032851}

此代码示例可为资产创建新的图像映射。 它使用由区域形状字符串常量确定的形状类型，并将句柄返回到新图像映射。

**请求**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**响应**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
