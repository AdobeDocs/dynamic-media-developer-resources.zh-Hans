---
description: 将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐合成图像（可能在缩放后也指定了scl=）。
solution: Experience Manager
title: 对齐
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# alig{#align}

将图像与视图对齐。 在wid=和hei=定义的视图矩形内对齐合成图像（可能在缩放后也指定了scl=）。

` align= *`水`*, *`平`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 霍里兹  </span> </span> </p> </td> 
  <td class="stentry"> <p>水平对齐（实数、-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 变态  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直对齐(real， -1.0...1.0) </p> </td> 
 </tr> 
</table>

指定`align=-1,-1`将复合图像的左上角与视图的左上角对齐，指定`align=1,1`将图像的右下角与视图的右下角对齐。 对于标准图像和缩略图请求，未被复合图像数据覆盖的视图的任何区域都将填充`bgc=`。

## 属性 {#section-3fbec8206fc944eda4746d8be84f3b41}

视图属性。 （`align=`还用于定义水印图像与应用水印的复合图像之间的对齐方式。） 无论当前图层设置如何，均适用。 如果仅指定`wid=`和`hei=`中的一个，并且当`fit=constrain`或`fit=stretch`时，将忽略。

## 默认 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，它将图像居中在视图矩形中。

## 示例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下请求适合`myImage`为200x200像素的视图矩形。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

如果`myImage`是正方形，则它将填充整个视图矩形。 如果`myImage`具有纵向长宽比，则它将缩放为200像素高，并在视图中水平居中。 如果`myImage`具有横向长宽比，则它将缩放为200像素宽，并与视图的上边缘对齐。 在所有情况下，返回的图像大小都是200x200像素；未被缩放`myImage`覆盖的任何空间都用`attribute::BkgColor`填充（指定bgc=以动态控制背景颜色）。

## 另请参阅 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , hei= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)fit= [, bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [水印](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
