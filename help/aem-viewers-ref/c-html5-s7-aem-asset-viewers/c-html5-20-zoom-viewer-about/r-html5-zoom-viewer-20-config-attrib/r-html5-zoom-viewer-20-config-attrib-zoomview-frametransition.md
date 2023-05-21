---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`持續時間`*[, *`間距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 無|淡化|幻燈片 </span> </p> </td> 
   <td colname="col2"> <p>指定套用到影格變更的效果型別。 屬性 <span class="codeph"> 無 </span> 代表無過渡；畫面格變更會立即發生。 屬性 <span class="codeph"> 淡化 </span> 表示舊影格和新影格之間的交叉淡化切換。 屬性 <span class="codeph"> 幻燈片 </span> 啟動轉變，舊框架滑出檢視，新框架滑入。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持續時間 </span> </span> </p> </td> 
   <td colname="col2"> <p>指定下列專案的持續時間（以秒為單位） <span class="codeph"> 淡化 </span> 或 <span class="codeph"> 幻燈片 </span> 切換效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間距 </span> </span> </p> </td> 
   <td colname="col2"> <p>中相鄰影格之間的間距 <span class="codeph"> 幻燈片 </span> 轉變，範圍從 <span class="codeph"> 0 </span> 到 <span class="codeph"> 1 </span> 和相對於元件的寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
