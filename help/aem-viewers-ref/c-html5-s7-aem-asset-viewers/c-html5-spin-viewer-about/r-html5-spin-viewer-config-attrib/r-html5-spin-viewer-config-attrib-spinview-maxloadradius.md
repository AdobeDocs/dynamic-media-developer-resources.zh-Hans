---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`高解析度`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示當「迴轉檢視」閒置時，在每個方向要預先載入影格數的上限。 值 <span class="codeph"> -1</span> 預先載入集中的所有影格。 預先載入的影格一律會以「迴轉檢視」最初載入的原始解析度顯示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高解析度</span></span> </p> </td> 
   <td colname="col2"> <p> 控制預先載入影格的品質。 當設定為 <span class="codeph"> 1</span> 影格會以高品質載入，符合元件的大小。 當設定為 <span class="codeph"> 0</span> 僅載入低解析度預覽拼貼。 </p> <p>以高解析度預先載入可改善一般使用者體驗，尤其是啟用自動迴轉時。 同時，它會導致啟動時間變慢和網路耗電量增加，因此請謹慎使用。 使用高解析度預先載入時，預先載入的影格一律為元件最初載入的原始解析度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
