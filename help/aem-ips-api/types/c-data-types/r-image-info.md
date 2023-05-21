---
description: 影像資產的屬性。
solution: Experience Manager
title: 影像資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 058c74b2-634c-49b9-88ab-ab72a030983c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 25%

---

# [!DNL ImageInfo]{#imageinfo}

影像資產的屬性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL originalPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>原始檔案的相對路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL originalFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>文件名. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> [!DNL optimizedPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS最佳化影像檔案的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL optimizedFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS最佳化的影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskPath]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像遮色片的路徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskFile]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>遮色片的檔案名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL width]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像寬度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL height]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像高度（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileSize]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>影像大小（位元組）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL resolution]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> <p>每英吋畫素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL sku]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>产品 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL description]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像說明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL comments]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>註解（已棄用）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL userData]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>與影像相關聯的使用者資訊（已棄用）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorX]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>以畫素為單位的水準錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL anchorY]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>畫素中的垂直錨點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>影像伺服器URL引數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL urlPostApplyModifier]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>串連到結尾的引數 <span class="codeph"> urlModifier</span>. 對影像伺服器發出命令的查詢字串格式引數清單。 值位於影像伺服器通訊協定指南中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL zoomTargets]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>縮放目標陣列（最多5個）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masks]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：遮色片陣列</span> </td> 
   <td colname="col3"> <p>遮罩陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageMaps]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageMapArray</span> </td> 
   <td colname="col3"> <p>影像地圖陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>
