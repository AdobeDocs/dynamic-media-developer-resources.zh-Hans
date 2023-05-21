---
title: 我的最愛檢視
description: 我的最愛檢視由一欄縮圖影像組成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# 我的最愛檢視{#favorites-view}

我的最愛檢視由一欄縮圖影像組成。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

我的最愛檢視容器外觀由以下CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7favoritesview
```

我的最愛檢視的位置和高度由檢視管理；在CSS中，只能定義寬度。

**我的最愛檢視的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 我的最愛檢視的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>檢視的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定100畫素寬、具有半透明灰色背景的「我的最愛」檢視。

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

我的最愛縮圖之間的間距由下列CSS類別選取器控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**我的最愛縮圖的CSS屬性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍的垂直邊界大小。 實際縮圖間距等於為設定的上下邊界的總和 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定十個畫素間距。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

使用下列CSS類別選取器可控制個別縮圖的外觀：

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**我的最愛縮圖的CSS屬性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 對應於使用者最近選取的縮圖。 當 `state="default"` 對應至其餘的縮圖。 和 `state="over"` 用於滑鼠游標暫留時。

範例 — 若要設定75 x 75畫素的縮圖，縮圖具有淺灰色的預設框線，以及選取的深灰色框線。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

縮圖示籤的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**我的最愛標籤的CSS屬性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 以14畫素Helvetica®字型設定標籤。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
