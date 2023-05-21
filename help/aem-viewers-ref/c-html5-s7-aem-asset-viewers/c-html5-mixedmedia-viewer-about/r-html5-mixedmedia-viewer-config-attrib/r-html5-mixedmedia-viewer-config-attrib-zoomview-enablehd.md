---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f6b25105-7b70-48f7-b3d6-e53110fd628b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 一律|永不|限制</span> </p> </td> 
   <td colname="col2"> <p> 啟用、限制或停用裝置的最佳化，其中 <span class="codeph"> devicePixelRatio</span> 大於 <span class="codeph"> 1</span>，也就是具有高密度顯示器的裝置，例如iPhone4和類似裝置。 如果啟用，則元件會限制IS影像請求的大小，彷彿裝置的畫素比僅為 <span class="codeph"> 1</span> 進而減少頻寬。 </p> <p>請參閱下列範例2。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用limit設定，元件僅會啟用指定上限的高畫素密度。 </p> <p>請參閱下列範例2。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

以下是在檢視器使用此設定屬性時的預期結果，且檢視器大小為1000 x 1000：

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>如果設定變數等於 </p> </th> 
   <th colname="col2" class="entry"> <p>结果 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 始终</span> </p> </td> 
   <td colname="col2"> <p>熒幕/裝置的畫素密度一律會計算。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果熒幕畫素密度= 1，則要求的影像為1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果熒幕畫素密度= 1.5，則要求的影像為1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果熒幕畫素密度= 2，則要求的影像為2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 从未</span> </p> </td> 
   <td colname="col2"> <p>它一律使用1的畫素密度，忽略裝置的HD功能。 因此，要求的影像一律為1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 限制&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>只有在產生的影像低於指定限制時，才會要求並提供裝置畫素密度。 </p> <p>限制數字會套用至寬度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果限制數量為1600，而畫素密度為1.5，則會提供1500 x 1500影像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制數量為1600，而畫素密度為2，則會提供1000 x 1000影像，因為2000 x 2000影像超過限制。 </p> </li> 
     </ul> </p> <p><b>最佳實務</b>：限制數量必須符合影像大小上限的公司設定。 因此，請將限制數量設定為等於公司影像大小上限設定。 </p> </td> 
  </tr> 
 </tbody> 
</table>
