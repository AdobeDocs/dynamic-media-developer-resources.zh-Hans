---
title: 設定指標
description: 設定指標是在觸控裝置上使用檢視器時，在色票上彩現的一系列點。 無法使用捲動按鈕時，圓點可協助使用者瀏覽縮圖頁面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---

# 設定指標{#set-indicator}

設定指標是在觸控裝置上使用檢視器時，在色票上彩現的一系列點。 無法使用捲動按鈕時，圓點可協助使用者瀏覽縮圖頁面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定指標的CSS屬性**

設定指示器容器的外觀是由下列CSS類別選取器所控制：

```
.s7zoomviewer .s7setindicator
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>設定指示器的十六進位格式的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要建立具有白色背景的設定指標：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個別設定指標點的外觀是由CSS類別選取器所控制：

`.s7zoomviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>設定指標點的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>設定指標點的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊界 </span> </p> </td> 
   <td colname="col2"> <p>以畫素為單位的左側邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂端邊界 </span> </p> </td> 
   <td colname="col2"> <p>上邊界（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右邊界 </span> </p> </td> 
   <td colname="col2"> <p>以畫素為單位的右邊界。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下方邊界 </span> </p> </td> 
   <td colname="col2"> <p>下方邊界（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>邊框半徑（畫素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>以十六進位格式表示的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指標點支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 對應至目前的縮圖頁面， `state="unselected"` 對應至預設點狀態。

範例 — 若要將設定指標點建立為15 x 15畫素，並具有2畫素水準邊界、5畫素上邊界、1畫素下邊界、12畫素半徑、#D5D3D3預設顏色和#939393個作用中顏色：

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
