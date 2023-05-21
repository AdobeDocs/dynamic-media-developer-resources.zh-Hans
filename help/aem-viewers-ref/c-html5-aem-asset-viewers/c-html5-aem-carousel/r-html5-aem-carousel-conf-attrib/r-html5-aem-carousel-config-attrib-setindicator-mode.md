---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 數值|虛線</span> </p> </td> 
   <td colname="col2"> <p> 設定設定指示的演算樣式。 </p> <p>當設定為 <span class="codeph"> 點狀 </span>時，元件會為所有頁面轉譯相同的指標。 </p> <p>當設定為 <span class="codeph"> 數值</span> 它會在每個指標元素內放置一個以1為基礎的頁碼。 </p> <p>此 <span class="codeph"> 數值</span> 具有觸控式輸入的裝置不支援操作模式。 相反地，元件使用 <span class="codeph"> 點狀</span> 在此類裝置上。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
