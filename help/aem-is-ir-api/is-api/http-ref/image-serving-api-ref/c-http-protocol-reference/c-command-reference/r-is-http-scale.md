---
description: 缩放图像。 相对于全分辨率图像按因子缩放图层源图像。
seo-description: 缩放图像。 相对于全分辨率图像按因子缩放图层源图像。
seo-title: scale
solution: Experience Manager
title: 缩放
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---


# scale{#scale}

缩放图像。 相对于全分辨率图像按因子缩放图层源图像。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>缩放因子（实数，大于0.0）。 </p></td> 
 </tr> 
</table>

`scale=1`时不应用缩放。 *`factor`* 小于1.0的缩小和大于1.0的放大源图像。

## 属性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

源图像/蒙版属性。 如果同时为当前图层指定`size=`，则忽略。 覆盖`res=`。 如果为`layer=comp`指定，则应用于层0。 如果图层未与图像或蒙版关联，则忽略。

## 默认 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定，则使用`res=`。 如果未指定`res=`，则使用图像时不进行缩放。

## 另请参阅 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
