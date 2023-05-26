---
description: 规范化坐标。 用于指定图像内的相对位置（如图像偏移量或裁切参数），这些参数已规范化为图像的大小。
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# coordN{#coordn}

规范化坐标。 用于指定图像内的相对位置（如图像偏移量或裁切参数），这些参数已规范化为图像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> 纽约</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> 纽约</span></span> </p></td> 
  <td class="stentry"> <p>标准化为图像大小的坐标偏移（实数、实数） </p></td> 
 </tr> 
</table>

正值向右下角移动。

在许多情况下，参考位置是图像的中心。 在这种情况下，0,0对应于图像的中心，-0.5，-0.5对应于左上角，0.5,0.5对应于右下角。

还用于指定图像大小或相对于图层0大小的矩形大小。 在这种情况下，值必须大于0。 0可能表示应使用特定的默认值。 1,1指定等于图层0的大小。
