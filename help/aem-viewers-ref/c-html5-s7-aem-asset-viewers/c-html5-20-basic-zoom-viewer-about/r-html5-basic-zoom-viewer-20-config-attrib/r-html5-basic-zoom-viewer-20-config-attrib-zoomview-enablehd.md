---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 启用、限制或禁用设备优化，其中 <span class="codeph"> devicePixelRatio</span> 大于 <span class="codeph"> 1</span>，即配备高密度显示器的设备，如iPhone4和类似设备。 如果激活，则组件限制IS图像请求的大小，就像设备只有像素比一样 <span class="codeph"> 1</span> 这样就可以减少带宽。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 数字</span> </span> </p> </td> 
   <td colname="col2"> <p> 如果使用limit设置，则组件启用高像素密度，但最多只能到指定的限制值。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选.

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

以下是在查看器中使用此配置属性且查看器大小为1000 x 1000时的预期结果：

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>如果设置的变量等于 </p> </th> 
   <th colname="col2" class="entry"> <p>结果 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 始终</span> </p> </td> 
   <td colname="col2"> <p>始终考虑屏幕/设备的像素密度。</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果屏幕像素密度= 1，则请求的图像为1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果屏幕像素密度= 1.5，则请求的图像为1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果屏幕像素密度= 2，则请求的图像为2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 从未</span> </p> </td> 
   <td colname="col2"> <p>它始终使用像素密度1，而忽略了设备的高清功能。 因此，请求的图像始终为1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 限制&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>仅当生成的图像低于指定限制时，才请求并提供设备像素密度。 </p> <p>限制数字适用于宽度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果极限数为1600，像素密度为1.5，则提供1500 x 1500图像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制数为1600，像素密度为2，则提供1000 x 1000图像，因为2000 x 2000图像超过限制。 </p> </li> 
     </ul> </p> <p> <b>最佳实践</b>：限制数字必须与最大大小图像的公司设置配合使用。 因此，请将限制数量设置为等于公司最大图像大小设置。 </p> </td> 
  </tr> 
 </tbody> 
</table>
