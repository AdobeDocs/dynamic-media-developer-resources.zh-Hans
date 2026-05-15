---
title: coordN
description: 规范化坐标。 用于指定图像内的相对位置，如图像偏移或裁切参数，这些参数已规范化为图像的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

规范化坐标。 用于指定图像内的相对位置，如图像偏移或裁切参数，这些参数已规范化为图像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>，<span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>规范化为图像大小的坐标偏移（实数、实数） </p></td> 
 </tr> 
</table>

正值向右下角移动。

通常，参照位置是图像的中心。 在这种情况下，`0,0`对应于图像的中心，`-0.5,-0.5`对应于左上角，`0.5,0.5`对应于右下角。

它还用于指定图像大小或相对于图层0大小的矩形大小。 在这种情况下，值必须大于0。 0表示应使用特定的默认值。 值为`1,1`指定大小等于图层0的大小。
