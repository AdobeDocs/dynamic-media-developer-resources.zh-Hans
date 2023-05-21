---
description: 標準化座標。 用於指定影像內的相對位置，例如影像位移或裁切引數，會標準化為影像的大小。
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

標準化座標。 用於指定影像內的相對位置，例如影像位移或裁切引數，會標準化為影像的大小。

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>， <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>標準化為影像大小的座標位移（實數、實數） </p></td> 
 </tr> 
</table>

正值會向右下方移動。

在許多情況下，參照位置是影像的中心。 在這種情況下，0,0會對應影像的中心，-0.5，-0.5對應至左上角，而0.5,0.5對應至右下角。

也可用來指定相對於圖層0大小的影像大小或矩形大小。 在此情況下，值必須大於0。 0可能表示應使用特定的預設值。 1,1指定等於圖層0的大小。
