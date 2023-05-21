---
title: PageView.zoomstep
description: PageView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 64cce312-c13b-49c7-af85-3349ff5c4322
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`步驟`*[, *`限制`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 設定以2的係數增加或減少解析度所需的放大和縮小動作數目。 每個縮放動作的解析度變化是每步階2^1。 設定為 <span class="codeph"> 0</span> 以使用單一縮放動作縮放至完整解析度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相對於完整解析度影像的最大縮放解析度。 預設值為 <span class="codeph"> 1.0</span>，這不會允許縮放超過完整解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-636d35a4791447039f1902973f568320}

可选.

## 默认 {#section-ad8a5fe2383e4c228bf177a41b53d921}

`1,1`

## 示例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
