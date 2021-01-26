---
description: 标准化坐标。 用于指定图像内的相对位置，如与图像大小标准化的图像偏移或裁剪参数。
seo-description: 标准化坐标。 用于指定图像内的相对位置，如与图像大小标准化的图像偏移或裁剪参数。
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# coordN{#coordn}

标准化坐标。 用于指定图像内的相对位置，如与图像大小标准化的图像偏移或裁剪参数。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>与图像大小(real、real)归一化的坐标偏移 </p></td> 
 </tr> 
</table>

正值朝右下方移动。

在许多情况下，参考位置是图像的中心。 在这种情况下，0,0对应于图像的中心，-0.5,-0.5对应于左上角，0.5,0.5对应于右下角。

还用于指定图像大小或相对于图层0大小的矩形大小。 在这种情况下，值必须大于0。 0可能表示应使用特定默认值。 1,1指定与层0的大小相等的大小。
