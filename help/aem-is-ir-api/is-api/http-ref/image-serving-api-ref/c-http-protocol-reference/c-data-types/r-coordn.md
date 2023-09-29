---
title: coordN
description: 规范化坐标。 用于指定图像内的相对位置，如图像偏移或裁切参数，这些参数已规范化为图像的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# coordN{#coordn}

规范化坐标。 用于指定图像内的相对位置，如图像偏移或裁切参数，这些参数已规范化为图像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> 纽约</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> 纽约</span></span> </p></td> 
  <td class="stentry"> <p>规范化为图像大小的坐标偏移（实数、实数） </p></td> 
 </tr> 
</table>

正值向右下角移动。

通常，参照位置是图像的中心。 在本例中， `0,0` 与图像的中心对应， `-0.5,-0.5` 左上角，并且 `0.5,0.5` 右下角。

它还用于指定图像大小或相对于图层0大小的矩形大小。 在这种情况下，值必须大于0。 0表示应使用特定的默认值。 值 `1,1` 指定等于图层0的大小。
