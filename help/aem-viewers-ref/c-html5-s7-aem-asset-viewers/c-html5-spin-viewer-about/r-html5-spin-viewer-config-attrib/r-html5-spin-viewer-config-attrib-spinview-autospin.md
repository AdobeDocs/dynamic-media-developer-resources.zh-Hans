---
title: SpinView.autospin
description: SpinView.autospin
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 6%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *`持續時間`*][, *`方向`*][, *`spin_num`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用自動迴轉動畫。 若要獲得最佳自動迴轉體驗，建議您透過設定來預先載入所有影格 <span class="codeph"> maxloadradius</span> 至 <span class="codeph"> -1</span>. 但是請注意，此設定會導致載入時間增加和頻寬使用率提高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 每次完全迴轉的秒數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 方向</span></span> </p> </td> 
   <td colname="col2"> <p> 迴轉方向 <span class="codeph"> 0</span> 用於向東旋轉和 <span class="codeph"> 1</span> 向西旋轉。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_num</span></span> </p> </td> 
   <td colname="col2"> <p> 自動迴轉停止前完成的完整迴轉次數。 數字是浮點數。 設定為 <span class="codeph"> -1</span> 進行無限自動迴轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
