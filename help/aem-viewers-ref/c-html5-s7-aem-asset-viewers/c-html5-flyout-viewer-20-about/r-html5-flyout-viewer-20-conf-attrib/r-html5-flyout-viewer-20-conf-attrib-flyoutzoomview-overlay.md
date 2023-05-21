---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 當彈出式視窗處於作用中狀態時，控制主檢視反白顯示外觀。 當設定為 <span class="codeph"> 0</span>，目前顯示在彈出式視窗中的區域會使用下列專案提供的樣式反白顯示： <span class="codeph"> .s7highlight</span> 或依據 <span class="codeph"> .s7cursor</span> CSS類別名稱(視 <span class="codeph"> 熒光模式</span> modifier)。 當設定為 <span class="codeph"> 1</span> 元件進入「反向」模式，目前檢視的區域為完全透明(如果是 <span class="codeph"> 熒光模式</span> 設為 <span class="codeph"> 反白顯示</span>)或樣式為 <span class="codeph"> .s7cursor</span> CSS類別名稱(大小寫 <span class="codeph"> 熒光模式</span> 設為 <span class="codeph"> 游標</span>)，但周圍區域會使用下列專案提供的樣式填滿： <span class="codeph"> .s7overlay</span> css類別名稱。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选.

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
