---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 906541bc-46dd-4a7c-8ee9-eb45ec3bd340
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.direction{#swatches-direction}

`[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td> <p> 指定在檢視中填入色票的方式。 </p> <p> <span class="codeph"> left </span> 設定由左至右的填色順序； </p> <p> <span class="codeph"> 右側 </span> 顛倒順序，因此檢視會由右至左、由上至下填入。 </p> <p>時間 <span class="codeph"> 自動 </span> 設定，則元件適用 <span class="codeph"> 右側 </span> locale設定為時的模式 <span class="codeph"> ja </span>；否則會使用left。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`direction=right`
