---
description: 标准化坐标。 用于指定图像内的相对位置，如与图像大小标准化的图像偏移或裁剪参数。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

标准化坐标。 用于指定图像内的相对位置，如与图像大小标准化的图像偏移或裁剪参数。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>、 <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>与图像大小（实、实）标准化的坐标偏移 </p></td> 
 </tr> 
</table>

正值朝右下方移动。

在很多情况下，参考位置是图像的中心。 在本例中，0,0对应于图像的中心，-0.5,-0.5对应于左上角，0.5,0.5对应于右下角。

还用于指定相对于图层0的大小的图像大小或矩形大小。 在这种情况下，值必须大于0。 0表示应使用特定的默认值。 1,1指定大小等于0层的大小。
