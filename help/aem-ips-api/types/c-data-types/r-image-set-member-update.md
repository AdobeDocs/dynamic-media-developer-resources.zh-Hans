---
description: 在此类型中，pageReset字段对RenderSet和目录图像资产类型有意义
solution: Experience Manager
title: ImageSetMemberupdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

在此类型中，pageReset字段对RenderSet和目录图像资产类型有意义：

* 对于`RenderSet`，`pageReset`表示新渲染视图/样本组的开始。

* 对于目录，`pageReset`表示新页面视图的开头。 通常，每个页面查看有2个页面图像，但您可以查看更多或更少的页面图像。

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
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 图像集成员数组中的资源句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3">重置页面。 <p>设置被忽略，<span class="codeph">图像集</span>和<span class="codeph">旋转集</span>的值强制为true。 </p></td> 
  </tr> 
 </tbody> 
</table>
