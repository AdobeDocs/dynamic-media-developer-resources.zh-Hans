---
description: '在此类型中，pageReset字段对RenderSet和Catalog图像资产类型有意义 '
seo-description: '在此类型中，pageReset字段对RenderSet和Catalog图像资产类型有意义 '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 6%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

在此类型中，pageReset字段对RenderSet和Catalog图像资产类型有意义：

* 对于`RenderSet`,`pageReset`指示新渲染视图/色板组的开始。

* 对于目录，`pageReset`指示新页面开始的视图。 通常，每个页面视图有2个页面图像，但您可以拥有更多或更少。

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
   <td colname="col3">重置页面。 <p>将忽略设置，并强制将<span class="codeph"> ImageSet</span>和<span class="codeph"> SpinSet</span>的值设置为true。 </p></td> 
  </tr> 
 </tbody> 
</table>

