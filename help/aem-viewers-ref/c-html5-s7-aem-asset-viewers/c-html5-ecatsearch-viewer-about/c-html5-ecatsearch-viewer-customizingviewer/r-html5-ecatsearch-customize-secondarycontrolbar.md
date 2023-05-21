---
title: 次要控制列
description: 次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，以及在CSS中提供時的「頁面指示器」。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# 次要控制列{#secondary-control-bar}

次要控制列是包含「第一頁」和「最後一頁」按鈕的矩形區域，以及在CSS中提供時的「頁面指示器」。

依預設，它只會顯示在行動電話上，在檢視器的底部。 它一律會佔用所有可用的檢視器寬度。 您可以透過CSS變更其相對於檢視器容器的顏色、高度和垂直位置。

次要控制列的外觀由下列CSS類別選取器控制：

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主要控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>次要控制列的背景色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定高72畫素且位於檢視器容器底部的灰色次要控制列。

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
