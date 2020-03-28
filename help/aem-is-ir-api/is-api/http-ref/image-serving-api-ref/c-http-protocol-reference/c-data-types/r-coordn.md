---
description: 标准化坐标。 用于指定图像内的相对位置，如图像偏移或裁剪参数，这些位置被归一化为图像的大小。
seo-description: 标准化坐标。 用于指定图像内的相对位置，如图像偏移或裁剪参数，这些位置被归一化为图像的大小。
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# coordN{#coordn}

标准化坐标。 用于指定图像内的相对位置，如图像偏移或裁剪参数，这些位置被归一化为图像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> nx <span class="varname"></span> , </span><span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> nx <span class="varname"></span> , </span><span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>与图像大小（实数、实数）标准化的坐标偏移 </p></td> 
 </tr> 
</table>

正值朝右下方移动。

在许多情况下，参考位置是图像的中心。 在这种情况下，0,0对应于图像的中心，-0.5,-0.5对应于左上角，0.5,0.5对应于右下角。

还用于指定图像大小或相对于图层0的矩形大小。 在这种情况下，值必须大于0。 0可能指示应使用特定默认值。 1,1指定与图层0相等的大小。
