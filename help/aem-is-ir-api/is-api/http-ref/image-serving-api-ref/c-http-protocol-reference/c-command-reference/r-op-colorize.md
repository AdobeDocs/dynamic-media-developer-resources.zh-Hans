---
description: 为图像着色。 在保留阴影和高光的同时为图像数据着色。
seo-description: 为图像着色。 在保留阴影和高光的同时为图像数据着色。
seo-title: op_colorize
solution: Experience Manager
title: op_colorize
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 4%

---


# op_colorize{#op-colorize}

为图像着色。 在保留阴影和高光的同时为图像数据着色。

` op_colorize= *``*[,off|norm[, *`色对比度`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> color </span> </p> </td> 
  <td class="stentry"> <p>替换RGB颜色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 關閉 </span> </p> </td> 
  <td class="stentry"> <p>禁用自动亮度补偿。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 规范  </span> </p> </td> 
  <td class="stentry"> <p>启用自动亮度补偿（默认）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 对比 </span> </p> </td> 
  <td class="stentry"> <p>对比度范围（实数0.100）；设置为0可保留输入对比度。 </p> </td> 
 </tr> 
</table>

第二个参数指定在着色之前是否应调整源图像的亮度。 指定`off`以禁用自动亮度补偿，或指定`norm`以自动调整亮度，使中值为50%强度。

将&#x200B;*`contrast`*&#x200B;值设置为0可保留输入图像的对比度范围，或指定值大于0的所需对比度范围。 值 100 将使对比度最大化。典型值可能介于30到70之间。

除了内置的亮度和对比度调整外，`op_brightness=`和`op_contrast=`还可用于进一步微调着色效果。

>[!NOTE]
>
>着色算法只使用图像数据中的亮度信息。 此转换为灰度很简单，不能进行颜色管理。 `op_colorize` 始终输出RGB数据，即使输入为灰度或CMYK。

## 属性 {#section-c0f8bd424b864153a1108f384939f55b}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

*`color`* 必须是RGB值；不支持 *`color`* 灰色或CMYK值。

如果关闭亮度补偿，则忽略&#x200B;*`contrast`*&#x200B;值。

*`color`* 假定存在于对应于像素类型的工作颜色空间中 *`color`*。*`color`* 如果图层图像在合并时具有不同的像素类型，则会精确转换图像。

在应用操作之前，CMYK图像将转换为RGB。

## 默认 {#section-0c3ea13efbac432c8970862d223e39b3}

`None`, for no colorization.对于自动亮度补偿和不更改对比度，第二个和第三个参数默认为`norm,0`。

## 示例 {#section-4c418d7b5e97409d9a448b8f08a1eab3}

在对图像图层着色之前动态调整亮度和对比度：

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

请改用自动亮度和对比度调整：

... `&op_colorize=a0b0c0,norm,50&`...

## 另请参阅 {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a),  [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d)，颜 [色管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
