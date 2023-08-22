---
title: scale
description: 缩放图像。 相对于全分辨率图像，按比例缩放图层源图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

缩放图像。 相对于全分辨率图像，按比例缩放图层源图像。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>缩放因子（实数，大于0.0）。 </p></td> 
 </tr> 
</table>

以下情况下不应用缩放 `scale=1`. *`factor`* 小于1.0的缩放，大于1.0的缩放，将放大源图像。

## 属性 {#section-3c7eb45527394fe79b1ddba6c1fcca09}

源图像/蒙版属性。 忽略条件 `size=` 也指定用于当前层。 覆盖 `res=`. 应用于层0（如果为指定） `layer=comp`. 如果图层未与图像或蒙版关联，则忽略。

## 默认 {#section-26e64904362342a5a62c5f6598f330c4}

如果未指定， `res=` 已使用。 如果 `res=` 未指定，不使用缩放使用图像。

## 另请参阅 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ， [大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
