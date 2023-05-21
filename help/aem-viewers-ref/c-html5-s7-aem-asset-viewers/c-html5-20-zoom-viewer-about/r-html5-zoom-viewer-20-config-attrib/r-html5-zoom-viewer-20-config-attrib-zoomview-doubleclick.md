---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以縮放動作的對應。 設定為 <span class="codeph"> 無 </span> 停用按兩下/點選縮放。 若設為 <span class="codeph"> 縮放 </span> 按一下影像可放大一個步階單位；按住CTRL鍵並按一下滑鼠可縮小一個步階單位。 設定為 <span class="codeph"> 重設 </span> 使得按一下影像即可將縮放重設為初始縮放等級。 對象 <span class="codeph"> zoomReset </span>，若目前縮放因數位於或超出指定限制會套用reset，否則會套用zoom。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`reset`  — 桌上型電腦； `zoomReset` 在觸控裝置上。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
