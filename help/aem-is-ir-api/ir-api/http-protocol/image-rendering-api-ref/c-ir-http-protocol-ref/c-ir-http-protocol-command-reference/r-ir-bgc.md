---
description: 背景颜色. 指定可着色纹理和颜色的减色。
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---

# bgc{#bgc}

背景颜色. 指定可着色纹理和颜色的减色。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色值。 </p></td> 
 </tr> 
</table>

图像渲染的纹理着色算法非常简单 — 从纹理像素的分量值中减去`bgc=`的分量值，再加入`color=`，最后将结果剪切到`0,0,0`和`255,255,255`。

对于纹理着色的典型用法，`bgc=`的值可能是纹理图像中最重要的或主要的颜色。 Dynamic Media图像创作提供了半自动工具，可从纹理图像中提取合理的`bgc=`颜色值。

当将纹理材料应用于非纹理可变的晕影对象时，如果未指定`color=`，则将`bgc=`作为前景颜色应用。

## 属性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材料属性。 被实色和机柜材料忽略。

## 默认 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果材料基于目录条目，则不 `bgc=808080` 然（中灰色）。

## 示例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

对纹理占主导RGB颜色120,34,193的服装织物进行着色：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另请参阅 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
