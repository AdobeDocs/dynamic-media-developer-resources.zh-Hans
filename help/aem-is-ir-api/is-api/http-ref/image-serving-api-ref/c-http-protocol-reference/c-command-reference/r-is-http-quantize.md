---
description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-description: 颜色量化。 为GIF输出转换指定颜色量化属性。
seo-title: 量化
solution: Experience Manager
title: 量化
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4e9c4807-59bc-4eb9-bcab-0bf0cfdf56d4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 3%

---


# 数量化{#quantize}

颜色量化。 为GIF输出转换指定颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 类型  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>指定调色板类型。 </p> <p>设置为<span class="codeph"> adaptive </span>可计算图像的最佳调色板。 </p> <p>设置为<span class="codeph"> web </span>或<span class="codeph"> mac </span>以选择预定义的调色板。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盘类型仅支持GIF和PNG8格式，但不支持GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {扩散|关闭}  </span> </p> <p>指定仿色选项。 </p> <p>对于Floyd-Steinberg错误扩散，设置为<span class="codeph">扩散</span> </p> <p>设置为<span class="codeph">关闭</span>以禁用仿色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色数(2-256) </p> <p>指定<span class="codeph">自适应</span>调色板中包含的颜色数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>以十六进制6格式的强制RGB颜色的逗号分隔列表 </p> <p>允许您指定要包含在<span class="codeph">自适应</span>调色板中的颜色。 如果指定的颜色数小于<span class="codeph"> <span class="varname"> numColors </span> </span>，则根据图像内容计算附加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前图层设置如何，均适用。 仅在`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`时使用。 否则忽略。

使用`*`colorList`*`指定的颜色必须由十六进制格式（请参见` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`）的RGB值组成，而不带“ `0x`”前缀。 不允许使用其他颜色说明符。 *`numColors`* 必须在2-256之间。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`调色板生成GIF缩略图，无仿色：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有键色透明度的双色调GIF，并强制颜色转换为黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，颜 [色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
