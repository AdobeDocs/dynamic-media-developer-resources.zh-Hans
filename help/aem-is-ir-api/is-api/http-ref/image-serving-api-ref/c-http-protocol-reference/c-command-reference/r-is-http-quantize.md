---
title: 量化
description: 颜色量化。 指定用于GIF输出转换的颜色量化属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 量化{#quantize}

颜色量化。 指定用于GIF输出转换的颜色量化属性。

` quantize= *`type`*[, *`抖动`*[, *`numColors`*[, *`颜色列表`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定调色板类型。 </p> <p>设置为 <span class="codeph"> 自适应 </span> 用于计算图像的最佳调色板。 </p> <p>设置为 <span class="codeph"> Web </span> 或 <span class="codeph"> mac </span> 以选择预定义的调色板。 </p> <p> <p>注意： <span class="codeph"> mac </span> 仅GIF和PNG8格式支持托盘类型，而GIFAlpha和PNG8 Alpha格式则不支持。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖动 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {扩散|关闭} </span> </p> <p>指定仿色选项。 </p> <p>设置为 <span class="codeph"> 扩散 </span> Floyd-Steinberg误差扩散 </p> <p>设置为 <span class="codeph"> 关闭 </span> 禁用仿色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色的数量(2-256) </p> <p>指定包含多少颜色 <span class="codeph"> 自适应 </span> 调色板。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 颜色列表 </span> </span> </p> </td> 
   <td colname="col2"> <p>以逗号分隔的强制十六进制RGB颜色列表 </p> <p>可让您指定要包含在 <span class="codeph"> 自适应 </span> 调色板。 如果指定的颜色数小于 <span class="codeph"> <span class="varname"> numColors </span> </span>，根据图像内容计算其他颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前图层设置如何，均适用。 仅在以下情况下使用 `fmt=gif`， `fmt=gif-alpha`， `fmt=png8`，或 `fmt=png8-alpha`. 否则，将忽略。

指定的颜色 *`colorList`* 必须包含十六进制6格式的RGB值(请参见 [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) 不含 `0x` 前缀。 不允许使用其他颜色说明符。 *`numColors`* 必须介于2-256之间。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用生成GIF缩略图 `web` 调色板和无抖动：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有关键色透明度的双调GIF，并强制将颜色转换为黑白色：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
