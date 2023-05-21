---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bd01ff03-fea7-42ad-aa99-72273f55bda0
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`direction=right`
