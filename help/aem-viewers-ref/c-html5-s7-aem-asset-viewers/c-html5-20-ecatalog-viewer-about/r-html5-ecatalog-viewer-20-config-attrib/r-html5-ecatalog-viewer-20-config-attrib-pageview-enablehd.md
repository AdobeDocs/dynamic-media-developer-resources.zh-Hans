---
title: PageView.enableHD
description: PageView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f03762f2-87db-4284-ba59-9ece8caa0d09
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 3%

---

# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 总是|从|不|限制</span> </p> </td> 
   <td colname="col2"> <p> 对以下设备启用、限制或禁用优化： <span class="codeph"> devicePixelRatio</span> 大于 <span class="codeph"> 1</span>，即具有高密度显示屏(如iPhone4和类似设备)的设备。 如果处于活动状态，则组件会限制IS图像请求的大小，如同设备仅具有像素比 <span class="codeph"> 1</span> 这样会降低带宽。 </p> <p>请参阅以下示例 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用限制设置，则组件仅启用高像素密度，而不超过指定限制。 </p> <p>请参阅以下示例。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-38b878e38caa439bb462d4fa637afdaa}

可选。

## 默认 {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## 示例 {#section-09433488774245d985acef6c0341ece0}

将此配置属性与查看器一起使用，且查看器大小为1000 x 1000时，预期结果如下：

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>如果设置的变量等于 </p> </th> 
   <th colname="col2" class="entry"> <p>结果 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 始终</span> </p> </td> 
   <td colname="col2"> <p>屏幕/设备的像素密度始终被计入在内。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>如果屏幕像素密度= 1，则请求的图像为1000 x 1000。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>如果屏幕像素密度= 1.5，则请求的图像为1500 x 1500。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>如果屏幕像素密度= 2，则请求的图像为2000 x 2000。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 从未</span> </p> </td> 
   <td colname="col2"> <p>它始终使用1的像素密度，并会忽略设备的HD功能。 因此，请求的映像始终为1000 x 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 限制&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>仅当所得图像低于指定限制时，才请求和提供设备像素密度。 </p> <p>限制编号适用于宽度或高度尺寸。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>如果限制数为1600，像素密度为1.5，则提供1500 x 1500的图像。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>如果限制数为1600，像素密度为2，则1000 x 1000图像会被提供，因为2000 x 2000图像超出限制。 </p> </li> 
     </ul> </p> <p><b>最佳实践</b>:限制编号必须与公司设置一起使用，以获得最大大小图像。 因此，请将限制数量设置为等于公司最大图像大小设置。 </p> </td> 
  </tr> 
 </tbody> 
</table>
