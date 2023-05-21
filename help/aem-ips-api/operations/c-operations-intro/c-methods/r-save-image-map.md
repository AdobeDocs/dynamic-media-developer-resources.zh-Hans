---
description: 建立新影像地圖或編輯現有地圖。
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 16%

---

# saveImageMap{#saveimagemap}

建立新影像地圖或編輯現有地圖。

语法

## 授權的使用者型別 {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取和寫入存取權。

## 参数 {#section-64f7f5fd8f954fba9fa30eeee556863a}

**輸入(saveImageMapParam)**

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
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 含有您要儲存之影像地圖的公司的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像地圖所屬影像資產的控點。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 影像地圖的控點。 如果為NULL，則建立影像地圖。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立或儲存的影像地圖名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 選擇區域形狀。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 區域 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 以逗號分隔定義區域的點清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 動作 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>此 <span class="codeph"> href </span> 與IPS介面中指定的影像地圖相關聯的值。 </p> <p>若要取得 <span class="codeph"> href </span> 值、按一下IPS介面中的影像、將URL複製並貼至此元素中，然後將IPS URL格式化為適當的URL。 例如， <span class="codeph"> 和 </span> 變成 <span class="codeph"> amp；(&amp;a) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像地圖清單中的順序（Z軸）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 已啟用 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**輸出(saveImageMapReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageMapHandle | `xsd:string` | 是 | 新影像地圖或已編輯影像地圖的控點。 |

## 示例 {#section-fdac488b640f427c8aa3d549c5032851}

此程式碼範例會為資產建立新的影像地圖。 它使用由區域形狀字串常數決定的形狀型別，並傳回新影像地圖的控點。

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
