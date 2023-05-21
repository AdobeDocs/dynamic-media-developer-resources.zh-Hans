---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 反白顯示|游標 </span> </p> </td> 
   <td colname="col2"> <p> 指定要使用的導覽框架型別。 當設定為 <span class="codeph"> 游標 </span>，元件會使用固定大小的參考游標。 桌上型電腦系統和觸控裝置可以有不同的游標藝術。 此功能的控制方式 <span class="codeph"> .s7cursor </span> CSS類別和 <span class="codeph"> input=mouse|touch </span> 屬性選擇器。 在桌上型電腦系統上，錨點會設定在游標區域的中央，而在觸控裝置上，錨點則設定在游標的下方。 當設定為 <span class="codeph"> 反白顯示 </span>時，元件會使用可變大小的導覽影格；影格的大小和形狀取決於縮放因數以及彈出式檢視的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> 設定反白顯示或游標在使用者啟動後淡入所需的時間（以秒為單位）。 淡入功能僅適用於觸控裝置，在桌上型電腦系統則會被元件忽略。 </p> <p>淡入會套用至下列UI元素：反白顯示框架、固定游標、覆蓋(如果是 <span class="codeph"> 覆蓋 </span> 引數已設為 <span class="codeph"> 1 </span>)。 彈出式檢視動畫只有在動畫完成時反白顯示/游標淡出後才開始。 沒有淡出動畫。 當使用者停用彈出式視窗時，對應的UI元素（游標、反白顯示和覆蓋）會立即隱藏。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|免費 </span> </p> </td> 
   <td colname="col2"> <p> 控制導覽框架位置。 </p> <p>若設為 <span class="codeph"> onimage </span>，導覽框架只能位於主檢視內的實際影像區域內。 </p> <p>若設為 <span class="codeph"> 免費 </span> 使用者可以將導覽框架移動至邏輯主檢視區域中的任一處，即使影像內容之外亦然。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
