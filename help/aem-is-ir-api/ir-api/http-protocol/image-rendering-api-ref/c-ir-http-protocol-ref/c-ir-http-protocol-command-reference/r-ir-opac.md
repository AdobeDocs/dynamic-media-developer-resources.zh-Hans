---
title: opac
description: 不透明度。 指定材质不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
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
