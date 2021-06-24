---
description: 将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐复合图像（可能是在缩放后，如果还指定了scl=）。
solution: Experience Manager
title: 对齐
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# 对齐{#align}

将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐复合图像（可能是在缩放后，如果还指定了scl=）。

` align= *``*, *`horizonvert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 霍里茨  </span> </span> </p> </td> 
  <td class="stentry"> <p>水平对齐（实数、-1.0..1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 变态  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直对齐（实数、-1.0..1.0） </p> </td> 
 </tr> 
</table>

指定`align=-1,-1`以将复合图像的左上角与视图的左上角对齐，指定`align=1,1`以将图像的右下角与视图的右下角对齐。 对于标准图像和缩略图请求，未被复合图像数据覆盖的视图的任何区域都将填充`bgc=`。

## 属性 {#section-3fbec8206fc944eda4746d8be84f3b41}

查看属性。 （`align=`还用于定义水印图像与应用水印的复合图像之间的对齐方式。） 无论当前的层设置如何，都适用。 如果只指定了`wid=`和`hei=`中的一个，并且当`fit=constrain`或`fit=stretch`时，则忽略。

## 默认 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，以在视图矩形中居中显示图像。

## 示例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下请求适合`myImage`到200x200像素视图矩形中。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果`myImage`正方形，则它将填充整个视图矩形。 如果`myImage`具有纵向长宽比，则其高度会缩放为200像素，并在视图中水平居中。 如果`myImage`具有横向长宽比，则它将缩放为200像素宽，并与视图的上边缘对齐。 在所有情况下，返回的图像大小都恰好为200x200像素；缩放的`myImage`未覆盖的任何空间都填充有`attribute::BkgColor`（指定bgc=以动态控制背景颜色）。

## 另请参阅 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
