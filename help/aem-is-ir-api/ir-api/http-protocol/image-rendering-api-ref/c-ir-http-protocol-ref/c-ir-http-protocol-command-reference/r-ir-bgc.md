---
title: bgc
description: 背景颜色. 指定可着色纹理和贴花的减色颜色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 5%

---

# bgc {#bgc}

背景颜色. 指定可着色纹理和贴花的减色颜色。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色的值。 </p></td> 
 </tr> 
</table>

图像渲染的纹理着色算法是直接的 —  `bgc=` 纹理像素值减去； `color=` 添加，最后将结果剪切到 `0,0,0` 和 `255,255,255`.

对于纹理上色的典型用途，值 `bgc=` 可能是纹理图像中最重要或最主要的颜色。 Dynamic Media图像创作提供了半自动的工具，可以合理提取 `bgc=` 纹理图像中的颜色值。

当纹理材料应用于不可纹理的晕影对象时， `bgc=` 在下列情况下应用为前景色 `color=` 未指定。

## 属性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材质属性。 已被纯色和机箱材料忽略。

## 默认 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果材料基于目录条目，否则 `bgc=808080` （中性灰色）。

## 示例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

为服装织物上色，其纹理具有主要的RGB颜色120、34、193：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另请参阅 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog：：基色](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ， [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
