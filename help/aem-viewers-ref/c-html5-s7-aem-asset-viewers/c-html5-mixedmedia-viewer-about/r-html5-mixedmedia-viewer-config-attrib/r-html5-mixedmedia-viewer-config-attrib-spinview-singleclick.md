---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按一下/點選以縮放動作的對應。 設定為 <span class="codeph"> 無 </span> 停用按一下/點選縮放。 若設為 <span class="codeph"> 縮放 </span> 按一下影像可放大一個步階單位；按住CTRL鍵並按一下滑鼠可縮小一個步階單位。 設定為 <span class="codeph"> 重設 </span> 使得按一下影像即可將縮放重設為初始迴轉等級。 對象 <span class="codeph"> zoomReset </span>，若目前縮放因數位於或超出指定限制會套用reset，否則會套用zoom。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 在桌上型電腦上； `none` 在觸控裝置上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
