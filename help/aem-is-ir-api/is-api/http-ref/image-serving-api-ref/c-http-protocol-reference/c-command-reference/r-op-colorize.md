---
title: op_colorize
description: 为图像着色。 为图像数据着色，同时保留阴影和高光。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1abbde32-867a-4596-a46b-12ec50d59170
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 3%

---

# op_colorize{#op-colorize}

为图像着色。 为图像数据着色，同时保留阴影和高光。

` op_colorize= *`颜色`*[,off|norm[, *`对比度`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">颜色</span> </p> </td> 
  <td class="stentry"> <p>替换RGB颜色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">折扣</span> </p> </td> 
  <td class="stentry"> <p>禁用自动亮度补偿。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">标准</span> </p> </td> 
  <td class="stentry"> <p>启用自动亮度补偿（默认）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">对比度</span> </p> </td> 
  <td class="stentry"> <p>对比度范围（实际0..100）；设置为0以保留输入对比度。 </p> </td> 
 </tr> 
</table>

第二个参数指定在着色之前是否应调整源图像的亮度。 指定`off`以禁用自动亮度补偿，或指定`norm`以自动调整亮度，使中间值达到50%强度。

将&#x200B;*`contrast`*&#x200B;值设置为0以保留输入图像的对比度范围，或者使用大于0的值指定所需的对比度范围。 值 100 将使对比度最大化。典型值可能介于30和70之间。

除了内置的亮度和对比度调整之外，`op_brightness=`和`op_contrast=`还可用于进一步微调着色效果。

>[!NOTE]
>
>彩色化算法仅使用图像数据中的亮度信息。 这种灰度转换非常简单，而且不受颜色管理。 `op_colorize`始终输出RGB数据，即使输入为灰度或CMYK也是如此。

## 属性 {#section-c0f8bd424b864153a1108f384939f55b}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。

*`color`*&#x200B;必须是RGB的值；不支持灰色或CMYK *`color`*&#x200B;值。

如果关闭亮度补偿，则忽略&#x200B;*`contrast`*&#x200B;值。

假设&#x200B;*`color`*&#x200B;存在于与&#x200B;*`color`*&#x200B;的像素类型对应的工作颜色空间中。 如果图层图像在合并时具有不同的像素类型，则精确转换&#x200B;*`color`*。

在应用操作之前，CMYK图像会转换为RGB。

## 默认 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`，表示无着色。 第二个和第三个参数默认为`norm,0`，用于自动亮度补偿且对比度不会更改。

## 示例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

在对图像图层上色之前，动态调整亮度和对比度：

... `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`...

请改用自动亮度和对比度调整：

... `&op_colorize=a0b0c0,norm,50&`...

## 另请参阅 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)，[op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a)，[op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
