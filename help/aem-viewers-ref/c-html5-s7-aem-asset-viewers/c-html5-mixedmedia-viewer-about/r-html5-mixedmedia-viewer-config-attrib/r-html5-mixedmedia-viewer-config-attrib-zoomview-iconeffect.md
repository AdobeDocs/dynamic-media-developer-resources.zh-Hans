---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`淡化`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用 <span class="codeph"> iconeffect</span> 當影像處於重設狀態時顯示在影像上方，這表示有可與影像互動的動作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定 <span class="codeph"> iconeffect</span> 即會出現，並重新出現。 值 <span class="codeph"> -1</span> 表示圖示永遠無限期地重新出現。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 淡化</span></span> </p> </td> 
   <td colname="col2"> <p>指定顯示或隱藏動畫的持續時間（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>設定「 」的秒數 <span class="codeph"> iconeffect</span> 在自動隱藏之前保持完全可見。 亦即，淡入動畫完成之後、淡出動畫開始之前的時間。 設定 <span class="codeph"> 0</span> 停用自動隱藏行為。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
