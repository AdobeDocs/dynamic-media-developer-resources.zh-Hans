---
description: 物质分辨率。 指定可重复纹理或倾斜图像的分辨率。
solution: Experience Manager
title: res
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# res{#res}

物质分辨率。 指定可重复纹理或倾斜图像的分辨率。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>决议；材料分辨率单位（通常为每英寸像素）（实数）。 </p> </td> 
 </tr> 
</table>

对于倾斜材料，如果同时指定了`size=`和`res=`，则`size=`将占上风。

## 属性 {#section-6a458ddc202f46e0b668c9f040a65cef}

材料属性。 被纯色材料忽略。 仅当还使用纹理时，才通过机柜和窗口覆盖材料。

## 默认 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`，则材料基于目录条目，否则，如果 `attribute::Resolution`未指 `res= is` 定或设置为小于或等于0的值，则为。

## 另请参阅 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[材料分辨率](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b),  [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
