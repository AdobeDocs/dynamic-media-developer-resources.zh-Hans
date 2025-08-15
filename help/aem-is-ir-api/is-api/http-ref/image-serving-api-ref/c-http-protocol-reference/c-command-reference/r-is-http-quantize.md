---
title: 量化
description: 颜色量化。 指定GIF输出转换的颜色量化属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 量化{#quantize}

颜色量化。 指定GIF输出转换的颜色量化属性。

` quantize= *`类型`*[, *`递色`*[, *`numColors`*[, *`颜色列表`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">类型</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定调色板类型。 </p> <p>设置为<span class="codeph">自适应</span>以计算图像的最佳调色板。 </p> <p>设置为<span class="codeph"> web </span>或<span class="codeph"> mac </span>以选择预定义的调色板。 </p> <p> <p>注意： <span class="codeph"> mac </span>托盘类型仅支持GIF和PNG8格式，不支持GIF-Alpha和PNG8-Alpha格式。</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">仿色</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {扩散|关闭} </span> </p> <p>指定仿色选项。 </p> <p>对于Floyd-Steinberg误差扩散，设置为<span class="codeph">扩散</span> </p> <p>设置为<span class="codeph">关闭</span>以禁用仿色。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>输出颜色的数量(2-256) </p> <p>指定<span class="codeph">最合适</span>调色板中包含的颜色数量。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">颜色列表</span> </span> </p> </td> 
   <td colname="col2"> <p>以逗号分隔的强制十六进制RGB颜色列表 </p> <p>允许您指定要包含在<span class="codeph">最合适</span>调色板中的颜色。 如果指定的颜色数小于<span class="codeph"> <span class="varname"> numColors </span> </span>，则根据图像内容计算其他颜色。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-8ab5035055b24b858270d260912a7f3d}

请求属性。 无论当前图层设置如何，它都适用。 仅在`fmt=gif`、`fmt=gif-alpha`、`fmt=png8`或`fmt=png8-alpha`时使用。 否则，将忽略。

使用&#x200B;*`colorList`*&#x200B;指定的颜色必须包含十六进制格式的RGB值（请参阅不带[前缀的](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md)color`0x`）。 不允许使用其他颜色说明符。 修饰符&#x200B;*`numColors`*&#x200B;必须为2-256。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用`web`调色板生成GIF缩略图且无仿色：

`http:// *`*服务器*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

将图像转换为具有键色透明度的双调GIF。 而且，强制颜色变为黑白：

`http:// *`*服务器*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
