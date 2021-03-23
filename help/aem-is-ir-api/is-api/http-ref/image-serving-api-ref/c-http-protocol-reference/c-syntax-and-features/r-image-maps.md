---
description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。
seo-description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。
seo-title: 图像映射
solution: Experience Manager
title: 图像映射
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# 图像映射{#image-maps}

IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。

通过`catalog::Map`或使用`map=`命令将源图像映射提供给IS，并使用`req=map`命令检索处理的映射。

图像映射由一个或多个HTML AREA元素组成，这些元素用“&lt;”和“>”正确分隔。 如果通过catalog::Map提供，则假定所有像素坐标值都在原始图像分辨率中，并且相对于（未修改）源图像的左上角。 通过`map=`命令提供时，坐标值假定为相对于图层左上角（在`rotate=`和`extend=`之后）的图层坐标。

>[!NOTE]
>
>此时不允许%坐标，处理可能不正确。

IS通过将空间变换（如缩放和旋转）应用于映射坐标，然后以适当的z顺序（从前到后）和适当的位置组合处理的图层映射，从每个组成图层的源图像映射生成复合图像映射。

与`req=map`（直接在请求中、通过目录模板或在`catalog::Modifier`字符串中）一起提供时，将考虑以下命令用于图像映射处理：

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

其他所有命令都会被有效忽略。

在处理`req=map`请求期间，可修改`AREA`的`SHAPE`和`COORDS`属性，不修改地传递该`AREA`元素的所有其它属性。 在大多数情况下，这包括将`SHAPE`值从`DEFAULT`更改为`RECT`（这也会添加`COORDS`属性）或更改`COORDS`值。

处理期间变为空的任何`AREA`元素将完全删除。 如果映射与`layer=comp`关联，则它将置于所有其他映射之后。 数据以文本形式返回，作为或多个HTML `AREA`元素。 空回复字符串表示指定对象不存在图像映射。

图层透明度不考虑用于地图处理。 完全透明的图层仍然可以具有与其关联的图像映射。 部分透明图层的映射不会被剪切到透明区域。

## 另请参阅 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , catalog: [:Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01规范](http://www.w3.org/TR/html401/)
