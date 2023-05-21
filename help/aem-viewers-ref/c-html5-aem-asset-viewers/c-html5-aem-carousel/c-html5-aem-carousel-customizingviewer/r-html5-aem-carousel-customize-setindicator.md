---
title: 設定指標
description: 設定指標是呈現在檢視器底部的一系列點。 它會顯示集合中的目前位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---

# 設定指標{#set-indicator}

設定指標是呈現在檢視器底部的一系列點。 它會顯示集合中的目前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**設定指標的CSS屬性**

設定指示器容器的外觀是由下列CSS類別選取器所控制：

```
.s7carouselviewer .s7setindicator
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

>[!NOTE]
>
>設定指標支援模式屬性選取器，可用來將不同的樣式套用至點狀和數值運算模式。 尤其是， `mode="numeric"` 與數值運算模式相對應； `mode="dotted"` 對應至預設點狀態。

例如，假設您要設定具有白色背景的設定指標：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

個別設定指標點的外觀是由CSS類別選取器所控制。 它適用於點狀和數值運算模式的專案。

`.s7carouselviewer .s7setindicator .s7dot`

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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字型色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>橫幅索引的垂直對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>橫幅索引的文字高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>設定指標專案支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 與集合中的目前元素相對應； `state="unselected"` 對應至預設專案狀態。

例如，假設您想要為桌上型電腦系統以點狀模式設定設定指標。 您希望它位於距離檢視器底部20畫素的位置。 而且，您想要未選取的點為黑色，透明度為50%，15 x 15畫素為7畫素圓角。 選取的點為黑色，透明度為90%，18 x 18畫素為9畫素圓角。 點之間的間距是五個畫素。

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
