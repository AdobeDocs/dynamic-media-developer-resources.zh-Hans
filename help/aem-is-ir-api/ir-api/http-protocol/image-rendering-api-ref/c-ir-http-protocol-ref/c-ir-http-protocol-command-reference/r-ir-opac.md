---
description: 不透明度. 指定材料不透明度。
seo-description: 不透明度. 指定材料不透明度。
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# opac{#opac}

不透明度. 指定材料不透明度。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>材料不透明度（百分比）;0...100 </p> </td> 
 </tr> 
</table>

以下材料／对象组合支持可变的不透明度：

* 应用于可纹理化的重叠对象的纯色和可重复纹理。
* 应用于窗覆盖框架对象的窗覆盖材料。
* 对可纹理化对象或壁式对象应用的褶皱。

如果材料包含具有Alpha渠道的图像，则 `opac=` 可以使用它使图像更透明，但不能更不透明。

## 属性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材料属性。 如果当前对象选择或材料不支持不透明度，则忽略此问题。

## 默认 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，对于完全不透明的材料(如果图像不包括alpha渠道)。
