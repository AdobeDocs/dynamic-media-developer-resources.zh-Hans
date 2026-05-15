---
description: 创建新图像映射或编辑现有映射。
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
TQID: 'https://experienceleague.adobe.com/ZSA0CvygWjE-RgySjcXudpqzrfaYZ2LUqeqbnlRLWbc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 244
ht-degree: 8%

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
>用户必须具有资产的读写访问权限。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含要保存的图像映射的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">资产句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射所属图像资源的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 图像映射的句柄。 如果为NULL，则创建图像映射。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 创建或保存的图像映射的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 区域形状的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">区域</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 以逗号分隔的定义区域的点列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">操作</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字符串</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>与IPS接口中指定的图像映射关联的<span class="codeph"> href </span>值。 </p> <p>要获取<span class="codeph"> href </span>值，请单击IPS界面中的图像，将URL复制并粘贴到此元素中，然后将IPS URL格式化为适当的URL。 例如，<span class="codeph">和</span>变为<span class="codeph"> &amp;amp； </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">位置</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：int </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射列表中的顺序（Z轴）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">已启用</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**输出(saveImageMapReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageMapHandle | `xsd:string` | 是 | 新图像映射或编辑后的图像映射的句柄。 |

## 示例 {#section-fdac488b640f427c8aa3d549c5032851}

此代码示例用于为资源创建新的图像映射。 它使用由区域形状字符串常量确定的形状类型，并向新图像映射返回一个句柄。

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
