---
description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。
seo-description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。
seo-title: 图像映射
solution: Experience Manager
title: 图像映射
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# 图像映射{#image-maps}

IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。

源图像映射通过`catalog::Map`或使用`map=`命令提供给IS，处理的映射使用`req=map`命令进行检索。

图像映射由一个或多个HTML AREA元素组成，该元素正确地用“&lt;”和“>”分隔。 如果通过catalog::Map提供，则假定所有像素坐标值都在原始图像分辨率中并且相对于（未修改的）源图像的左上角。 当通过`map=`命令提供时，坐标值假定为相对于层左上角的层坐标（在`rotate=`和`extend=`之后）。

>[!NOTE]
>
>此时不允许%坐标，处理可能不正确。

IS通过将空间变换（如缩放和旋转）应用到地图坐标，然后以适当的z顺序（从前到后）和适当的位置将处理的图层地图组合，从每个组成层的源图像地图生成复合图像地图。

当与`req=map`（直接在请求中、通过目录模板或在`catalog::Modifier`字符串中提供）一起提供时，将考虑以下命令进行图像映射处理：

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

所有其他命令都会被有效忽略。

在处理`req=map`请求期间，可修改`AREA`的`SHAPE`和`COORDS`属性，不修改`AREA`元素的所有其它属性。 在大多数情况下，这包括将`SHAPE`值从`DEFAULT`更改为`RECT`（这也会添加`COORDS`属性），或更改`COORDS`值。

处理过程中变为空的任何`AREA`元素将完全删除。 如果映射与`layer=comp`关联，则它将位于所有其他映射的后面。 数据以文本形式返回，格式为一个或多个HTML `AREA`元素。 空的回复字符串表示指定对象不存在图像映射。

图层透明度不考虑用于地图处理。 完全透明的图层仍然可以具有与其关联的图像映射。 部分透明层的映射不会被剪切到透明区域。

## 另请参阅 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [目录：](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md):Map [,HTML 4.01规范](http://www.w3.org/TR/html401/)
