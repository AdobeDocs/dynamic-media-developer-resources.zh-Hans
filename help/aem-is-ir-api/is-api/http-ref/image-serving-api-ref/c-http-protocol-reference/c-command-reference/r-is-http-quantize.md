---
description: 颜色量化。 指定GIF输出转换的颜色量化属性。
solution: Experience Manager
title: 数量
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# 数量化{#quantize}

颜色量化。 指定GIF输出转换的颜色量化属性。

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 类型  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac}  </span> </p> <p>指定调板类型。 </p> <p>设置为<span class="codeph"> adaptive </span>可计算图像的最佳调色板。 </p> <p>设置为<span class="codeph"> web </span>或<span class="codeph"> mac </span>以选择预定义的调色板。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盘类型仅支持GIF和PNG8格式，但不支持GIF-Alpha和PNG8-Alpha格式。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 抖动  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {massure|off}  </span> </p> <p>指定仿色选项。 </p> <p>对于Floyd-Steinberg错误扩散，设置为<span class="codeph">扩散</span> </p> <p>设置为<span class="codeph">关闭</span>以禁用仿色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色数(2-256) </p> <p>指定<span class="codeph">自适应</span>调板中包含的颜色数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
   <td colname="col2"> <p>以逗号分隔的十六进制6格式强制RGB颜色列表 </p> <p>允许您指定要包含在<span class="codeph">自适应</span>调板中的颜色。 如果指定的颜色数小于<span class="codeph"> <span class="varname"> numColors </span> </span>，则根据图像内容计算附加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前图层设置如何，均适用。 仅在`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`时使用。 否则忽略。

使用`*`colorList`*`指定的颜色必须由十六进制6格式（请参阅` [color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)`）的RGB值组成，且没有“ `0x`”前缀。 不允许使用其他颜色说明符。 *`numColors`* 必须在2-256之间。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`调板生成GIF缩览图，无仿色：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有键控颜色透明度的双色调GIF，并将颜色强制为黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
