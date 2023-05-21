---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預先載入行為。 </p> <p>當設定為 <span class="codeph"> -1</span> 當處於閒置狀態時，元件會預先載入所有目錄影格。 </p> <p> 當設定為 <span class="codeph"> 0</span> 元件僅載入目前可見的影格、上一個影格和下一個影格。 </p> <p>設定 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定義在閒置狀態中預先載入目前顯示影格周圍的不可見影格數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选.

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
