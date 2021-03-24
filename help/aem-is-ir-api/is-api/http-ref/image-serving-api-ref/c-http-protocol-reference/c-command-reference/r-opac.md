---
description: 调整图像不透明度。 允许降低图像、文本、纯色或效果图层的前景不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---


# opac{#opac}

调整图像不透明度。 允许降低图像、文本、纯色或效果图层的前景不透明度。

`opac= *`不透`*[, *`明填充不透明度`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明</span> </p> </td> 
  <td class="stentry"> <p>主不透明度(0...100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>填充不透明度(0...100 int)。 </p></td> 
 </tr> 
</table>

图像图层的前景不透明度由图层蒙版或图像的Alpha渠道决定，或者，如果两者都不存在，则为100%。 文本图层的前景不透明度为100%，纯色图层的前景不透明度由`color=`设置。

`opac=` 除了纯色和效果图层(设置 `color=` 为 `bgColor=`)的前景区域外，永远不要修改用或填充的区域的不 `color=`透明度。

当在图像、文本或纯色图层中指定时，*`opacity`*&#x200B;将应用整个图层，包括所有关联的效果图层，而&#x200B;*`fillOpacity`*&#x200B;仅应用于主图层内容。 当在效果图层中指定时，*`opacity`*&#x200B;将应用于效果图层，而&#x200B;*`fillOpacity`*&#x200B;将被忽略。

主图层内容的有效不透明度为(*`opacity`* * *`fillOpacity`* / 100)。 效果图层的有效不透明度为（主&#x200B;*`opacity`* *效果&#x200B;*`opacity`* / 100）。

## 属性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。

## 默认 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，以保持图层不透明度不变。

## 示例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

此示例中的文本不透明度为90*70/100=63%，效果图层不透明度为90*50/100=45%。

## 另请参阅 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
