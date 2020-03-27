---
description: 将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐合成图像（可能是在缩放后，如果也指定了scl=）。
seo-description: 将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐合成图像（可能是在缩放后，如果也指定了scl=）。
seo-title: 对齐
solution: Experience Manager
title: 对齐
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐合成图像（可能是在缩放后，如果也指定了scl=）。

` align= *`水`*, *`平`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span></span> </p> </td> 
  <td class="stentry"> <p>水平对齐（实数、-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>垂直对齐(real, -1.0...1.0) </p> </td> 
 </tr> 
</table>

指 `align=-1,-1` 定将复合图像的左上角与视图的左上角对齐，指定 `align=1,1` 将图像的右下角与视图的右下角对齐。 对于标准图像和缩略图请求，视图中未被复合图像数据覆盖的任何区域都会填充 `bgc=`。

## 属性 {#section-3fbec8206fc944eda4746d8be84f3b41}

视图属性。 (还 `align=` 用于定义水印图像与应用了水印的复合图像之间的对齐方式。)无论当前图层设置如何，均可应用。 如果仅指定和之一， `wid=` 且 `hei=` 在或时，则忽 `fit=constrain` 略该值 `fit=stretch`。

## 默认 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，它将图像居中在视图矩形中。

## 示例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下请求适 `myImage` 合200x200像素的视图矩形。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果 `myImage` 正方形，则填充整个视图矩形。 如果 `myImage` 有纵向长宽比，则将其缩放为200像素高，并在视图中水平居中。 如 `myImage` 果具有横向长宽比，则将其缩放为200像素宽并与视图的顶边对齐。 在所有情况下，返回的图像大小都恰好为200x200像素；缩放后未覆盖的任何空 `myImage` 间将填充 `attribute::BkgColor` （指定bgc=以动态控制背景颜色）。

## 另请参阅 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , hei= [, fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), bgc= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
