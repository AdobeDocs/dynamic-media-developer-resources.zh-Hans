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


# Image maps{#image-maps}

IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。

源图像映射通过命令或通过命 `catalog::Map` 令提供给 `map=` IS，并且使用命令检索处理的映 `req=map` 射。

图像映射由一个或多个HTML AREA元素组成，该元素正确地用“&lt;”和“>”分隔。 如果通过catalog::Map提供，则假定所有像素坐标值都在原始图像分辨率中，并且相对于（未修改的）源图像的左上角。 当通过命 `map=` 令提供时，坐标值被假定为相对于层左上角（在和之后）的层坐 `rotate=` 标 `extend=`。

>[!NOTE]
>
>此时不允许%坐标，处理可能不正确。

IS通过将空间变换（如缩放和旋转）应用到地图坐标，然后以适当的z顺序（从前到后）和适当的位置将处理的图层地图组合，从每个组成层的源图像地图生成复合图像地图。

当与(直接在请求中、通过目录模板或字符串中 `req=map` 提供)一起提供时，将考虑以下命令进行图像 `catalog::Modifier` 映射处理：

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

在处 `SHAPE` 理请求 `COORDS` 期间，可以修改元件的属性和属 `AREA` 性，元件的所有其它属性都 `req=map``AREA` 不进行修改。 在大多数情况下，这涉 `SHAPE` 及将值 `DEFAULT` 从更 `RECT` 改为(这也会添加 `COORDS` 属性)或更改 `COORDS` 值。

在处 `AREA` 理过程中变为空的任何元素将完全删除。 如果地图与其关联，则 `layer=comp` 它将被置于所有其他地图的后面。 以文本形式返回数据作为一个或多个HTML `AREA` 元素。 空的回复字符串表示指定对象不存在图像映射。

图层透明度不考虑用于地图处理。 完全透明的图层仍然可以具有与其关联的图像映射。 部分透明层的映射不会被剪切到透明区域。

## 另请参阅 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01规范](http://www.w3.org/TR/html401/)
