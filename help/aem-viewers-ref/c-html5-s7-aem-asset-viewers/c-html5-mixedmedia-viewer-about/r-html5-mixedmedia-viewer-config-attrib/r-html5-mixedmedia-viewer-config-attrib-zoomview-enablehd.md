---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f6b25105-7b70-48f7-b3d6-e53110fd628b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 允许、限制或禁止对<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备进行优化，这些设备是指具有高密度显示的设备，如iPhone4和类似设备。 如果处于活动状态，则组件会限制IS图像请求的大小，就像设备只有<span class="codeph"> 1</span>的像素比一样，这样会减少带宽。 </p> <p>请参阅下面的示例2。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅在指定限制内启用高像素密度。 </p> <p>请参阅下面的示例2。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

当将此配置属性与查看器一起使用，且查看器大小为1000 x 1000时，预期结果如下：

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>如果设置的变量等于 </p> </th> 
   <th colname="col2" class="entry"> <p>结果 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">始终</span> </p> </td> 
   <td colname="col2"> <p>始终考虑屏幕/设备的像素密度。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果屏幕像素密度= 1，则请求的图像为1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果屏幕像素密度= 1.5，则请求的图像为1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果屏幕像素密度= 2，则请求的图像为2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">从不</span> </p> </td> 
   <td colname="col2"> <p>它始终使用像素密度1，忽略设备的高清功能。 因此，请求的图像始终为1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">限制&lt;数字&gt;</span> </p> </td> 
   <td colname="col2"> <p>仅当生成的图像低于指定限制时，才请求和提供设备像素密度。 </p> <p>限制数字适用于宽度或高度维度。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果限制数为1600，像素密度为1.5，则提供1500 x 1500图像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制数为1600，像素密度为2，则提供1000 x 1000图像，因为2000 x 2000图像超出限制。 </p> </li> 
     </ul> </p> <p><b>最佳实践</b>：限制数字必须与最大大小图像的公司设置一起使用。 因此，请将限制数量设置为等于公司最大图像大小设置。 </p> </td> 
  </tr> 
 </tbody> 
</table>
