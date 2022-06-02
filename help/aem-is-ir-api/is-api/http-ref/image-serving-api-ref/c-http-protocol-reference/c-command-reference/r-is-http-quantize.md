---
title: 数量
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 3%

---

# 数量{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *`type`*[, *`抖动`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定调色板类型。 </p> <p>设置为 <span class="codeph"> 自适应 </span> 以计算图像的最佳调色板。 </p> <p>设置为 <span class="codeph"> web </span> 或 <span class="codeph"> mac </span> 来选择预定义的调色板。 </p> <p> <p>注意：的 <span class="codeph"> mac </span> 托盘类型仅支持GIF和PNG8格式，而不支持GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖动 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {dusse|off} </span> </p> <p>指定抖动选项。 </p> <p>设置为 <span class="codeph"> 扩散 </span> Floyd-Steinberg误差扩散 </p> <p>设置为 <span class="codeph"> 关闭 </span> 禁用抖动。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色的数量(2-256) </p> <p>指定 <span class="codeph"> 自适应 </span> 面板。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>以十六进制6格式的强制RGB颜色列表（以逗号分隔） </p> <p>允许您指定要包含在 <span class="codeph"> 自适应 </span> 面板。 如果指定的颜色数小于 <span class="codeph"> <span class="varname"> numColors </span> </span>，则会根据图像内容计算其他颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前的层设置如何，都适用。 仅在 `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`或 `fmt=png8-alpha`. 否则，将忽略。

指定的颜色 *`colorList`* 必须包含十六进制6格式的RGB值(请参阅 [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) 无 `0x` 前缀。 不允许使用其他颜色说明符。 *`numColors`* 必须在2到256之间。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用生成GIF缩略图 `web` 调色板和无抖动：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有键色透明度的双色调GIF，并强制将颜色转换为黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
