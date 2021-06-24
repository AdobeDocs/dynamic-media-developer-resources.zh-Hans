---
description: '在此类型中，pageReset字段对于RenderSet和Catalog图像资产类型有意义 '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic，SDK/API，图像集
role: Developer,Administrator
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 7%

---

# ImageSetMemberUpdate{#imagesetmemberupdate}

在此类型中，pageReset字段对于RenderSet和目录图像资产类型有意义：

* 对于`RenderSet`, `pageReset`表示新呈现视图/色板组的开始。

* 对于目录，`pageReset`表示新页面查看的开始。 通常，每个页面查看有2个页面图像，但您可以拥有更多或更少。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 图像集成员数组中的资产句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">重置页面。 <p>将忽略设置，并将<span class="codeph"> ImageSet</span>和<span class="codeph"> SpinSet</span>的值强制设置为true。 </p></td> 
  </tr> 
 </tbody> 
</table>
