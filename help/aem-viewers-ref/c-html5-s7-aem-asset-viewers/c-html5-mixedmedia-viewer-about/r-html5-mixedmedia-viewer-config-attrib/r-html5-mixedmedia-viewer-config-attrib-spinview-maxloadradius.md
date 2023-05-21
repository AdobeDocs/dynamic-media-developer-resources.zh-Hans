---
title: SpinView.maxloadradius
description: 表示當「迴轉檢視」閒置時，在每個方向要預先載入影格數的上限。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

表示當「迴轉檢視」閒置時，在每個方向要預先載入影格數的上限。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`高解析度`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 值 <span class="codeph"> -1</span> 預先載入集中的所有影格。 預先載入的影格一律會以「迴轉檢視」最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高解析度</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預先載入影格的品質。 </p> <p>當設定為 <span class="codeph"> 1</span> 影格會以高品質載入，符合元件的大小。 </p> <p>當設定為 <span class="codeph"> 0</span> 僅載入低解析度預覽拼貼。</p> <p>以高解析度預先載入可改善使用者的體驗，尤其是在啟用自動迴轉的情況下。 同時，這會使啟動時間變慢且耗用更多網路，因此應謹慎使用。 使用高解析度預先載入時，預先載入的影格一律為元件最初載入的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
