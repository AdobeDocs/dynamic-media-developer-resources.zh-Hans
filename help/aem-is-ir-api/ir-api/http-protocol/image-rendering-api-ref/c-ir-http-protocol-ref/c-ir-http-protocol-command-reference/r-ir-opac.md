---
title: opac
description: 不透明度。 指定材质不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 0%

---

# opac{#opac}

不透明度。 指定材质不透明度。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>材质不透明度（百分比）；0...100 </p> </td> 
 </tr> 
</table>

以下材料/对象组合支持可变不透明度：

* 应用于纹理重叠对象的纯色和可重复纹理。
* 应用于窗饰框架对象的窗饰材料。
* 应用于文本对象或墙壁对象的标记。

如果材质包含具有Alpha通道的图像，则可以使用`opac=`使图像更透明，而不是更不透明。

## 属性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材质属性。 如果当前对象选择或材料不支持不透明度，则忽略。

## 默认 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，对于完全不透明的材料（如果图像不包含Alpha通道）。
