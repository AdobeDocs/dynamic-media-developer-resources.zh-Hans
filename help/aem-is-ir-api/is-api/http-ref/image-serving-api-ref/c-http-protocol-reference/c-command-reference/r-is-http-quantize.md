---
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
solution: Experience Manager
title: 数量
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 3%

---

# 数量{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>指定调色板类型。 </p> <p>设置为<span class="codeph">自适应</span>可计算图像的最佳调色板。 </p> <p>设置为<span class="codeph"> web </span>或<span class="codeph"> mac </span>以选择预定义的调色板。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盘类型仅支持GIF和PNG8格式，而不支持GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {dusse|off}  </span> </p> <p>指定抖动选项。 </p> <p>对于Floyd-Steinberg误差扩散，设置为<span class="codeph">扩散</span> </p> <p>设置为</span>的<span class="codeph">可禁用抖动。 </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色的数量(2-256) </p> <p>指定<span class="codeph">自适应</span>调色板中包含的颜色数量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>以十六进制6格式的强制RGB颜色列表（以逗号分隔） </p> <p>允许您指定要包含在<span class="codeph">自适应</span>调色板中的颜色。 如果指定的颜色数小于<span class="codeph"> <span class="varname"> numColors </span> </span>，则会根据图像内容计算其他颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前的层设置如何，都适用。 仅在`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`时使用。 否则，将忽略。

使用`*`colorList`*`指定的颜色必须由RGB值组成，其格式为十六进制6（请参阅` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`），且不带“ `0x`”前缀。 不允许使用其他颜色说明符。 *`numColors`* 必须在2到256之间。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`面板生成GIF缩略图，且无抖动：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有键色透明度的双色调GIF，并强制将颜色转换为黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，颜 [色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
