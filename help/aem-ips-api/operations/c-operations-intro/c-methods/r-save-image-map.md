---
description: 创建新的图像映射或编辑现有的映射。
seo-description: 创建新的图像映射或编辑现有的映射。
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 15%

---


# saveImageMap{#saveimagemap}

创建新的图像映射或编辑现有的映射。

语法

## 授权用户类型{#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

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
   <td colname="col4"> 包含要保存的图像映射的公司的手柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射所属的图像资产的手柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 图像映射的手柄。 如果为NULL，则创建图像映射。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称  </span> </span> </td> 
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
   <td colname="col4"> 用逗号分隔的点列表，定义区域。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 行动  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>与IPS接口中指定的图像映射关联的<span class="codeph"> href </span>值。 </p> <p>要获取<span class="codeph"> href </span>值，请单击IPS接口中的图像，将URL复制并粘贴到此元素中，然后将IPS URL格式化为正确的URL。 例如，<span class="codeph">和</span>变为<span class="codeph"> &amp;</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 位置  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 图像映射列表（Z轴）的顺序。 </td> 
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
| `*`imageMapHandle`*` | `xsd:string` | 是 | 新图像或已编辑图像映射的手柄。 |

## 示例 {#section-fdac488b640f427c8aa3d549c5032851}

此代码示例为资产创建新的图像映射。 它使用由区域形状字符串常量确定的形状类型，并将手柄返回到新图像映射。

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

