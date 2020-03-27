---
description: 背景颜色. 为可着色的纹理和装饰指定减色颜色。
seo-description: 背景颜色. 为可着色的纹理和装饰指定减色颜色。
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

背景颜色. 为可着色的纹理和装饰指定减色颜色。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色值。 </p></td> 
 </tr> 
</table>

图像渲染的纹理着色算法非常简单——将纹理像素的分量值相减 `bgc=` ，再加 `color=` ，最后将结果剪切到 `0,0,0` 和 `255,255,255`。

对于纹理着色的典型应用，纹理图 `bgc=` 像中最重要的颜色或主色的值可能是。 Scene7图像创作提供了从纹理图像中提取合理颜色 `bgc=` 值的半自动工具。

当将纹理材料应用于非纹理暗角对象时，如 `bgc=` 果未指定，则将作为前景色 `color=` 应用纹理材料。

## 属性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材料属性。 被纯色和机柜材料忽略。

## 默认 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果材料基于目录条目，则为中性 `bgc=808080` 灰色。

## 示例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

对其纹理具有主要RGB颜色120,34,193的服装织物进行着色：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另请参阅 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
