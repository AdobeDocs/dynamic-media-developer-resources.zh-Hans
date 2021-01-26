---
description: 物质分辨率。 指定可重复纹理或贴体图像的分辨率。
seo-description: 物质分辨率。 指定可重复纹理或贴体图像的分辨率。
seo-title: res
solution: Experience Manager
title: res
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---


# res{#res}

物质分辨率。 指定可重复纹理或贴体图像的分辨率。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>决议；材料分辨率单位（通常为每英寸像素）（实数）。 </p> </td> 
 </tr> 
</table>

如果是倾斜材料，则如果同时指定了`size=`和`res=`，则`size=`优先。

## 属性 {#section-6a458ddc202f46e0b668c9f040a65cef}

材料属性。 被纯色材料忽略。 只有在同时使用纹理时，才能通过机箱和窗口覆盖材料。

## 默认 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`，如果材料基于目录条目，则 `attribute::Resolution`否 `res= is` 则，如果未指定或设置为小于或等于0的值。

## 另请参阅 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Material Resolution](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b) [, ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)size= [, ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7)catalog::Resolution [, attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
