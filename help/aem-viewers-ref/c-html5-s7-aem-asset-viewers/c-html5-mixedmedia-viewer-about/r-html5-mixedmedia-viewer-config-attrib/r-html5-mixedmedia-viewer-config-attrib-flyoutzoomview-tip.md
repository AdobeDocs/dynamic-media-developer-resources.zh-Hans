---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持續時間`*[, *`count`*][, *`淡化`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文字在隱藏前顯示的秒數。 當設定為 <span class="codeph"> -1</span>，則一律會顯示訊息，即使使用者啟用彈出式視窗亦然。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定檢視集合中新影像時顯示文字的次數。 值 <span class="codeph"> -1</span> 表示檢視影像集中的任何影像時，一律會顯示文字。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡化</span></span> </p> </td> 
   <td colname="col2"> 指定文字出現或消失時所發生之淡化動畫的持續時間。 值 <span class="codeph"> 0</span> 表示無淡化切換。 </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
