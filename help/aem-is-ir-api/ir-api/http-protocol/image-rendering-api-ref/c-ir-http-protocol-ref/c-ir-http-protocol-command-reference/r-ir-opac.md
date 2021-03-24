---
description: 不透明度. 指定材质不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# opac{#opac}

不透明度. 指定材质不透明度。

` opac= *`瓦尔`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 瓦尔  </span> </p> </td> 
  <td class="stentry"> <p>材料不透明度（百分比）；0..100 </p> </td> 
 </tr> 
</table>

以下材料/对象组合支持可变的不透明度：

* 应用于可纹理重叠对象的纯色和可重复纹理。
* 应用于覆盖框架对象的窗口覆盖材料。
* 应用于可文本化对象或壁对象的贴图。

如果材料包含具有Alpha渠道的图像，则`opac=`可用于使图像更透明，但不是更不透明。

## 属性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材料属性。 如果当前对象选择或材料不支持不透明度，则忽略。

## 默认 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，对于完全不透明的材料(如果图像不包含alpha渠道)。
