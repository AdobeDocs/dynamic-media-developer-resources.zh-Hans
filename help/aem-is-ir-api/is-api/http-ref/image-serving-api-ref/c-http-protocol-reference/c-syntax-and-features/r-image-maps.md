---
description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还对图像映射提供了有限支持。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 图像映射{#image-maps}

IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还对图像映射提供了有限支持。

源图像映射通过 `catalog::Map` 或 `map=` 命令，并使用 `req=map` 命令。

图像映射由一个或多个HTMLAREA元素组成，正确分隔为“&lt;”和“>”。 如果通过catalog::Map提供，则所有像素坐标值都假定在原始图像分辨率中，并且相对于（未修改）源图像的左上角。 当通过 `map=` 命令，则坐标值被假定为相对于层左上角的层坐标（之后） `rotate=` 和 `extend=`)。

>[!NOTE]
>
>此时不允许%坐标，并且可能处理不正确。

IS通过将空间变换（如缩放和旋转）应用到映射坐标，然后以适当的z顺序（前后）和适当的定位来组装处理的层映射，从每个组成层的源图像映射生成复合图像映射。

如果与 `req=map` (通过目录模板直接在请求中或在 `catalog::Modifier` 字符串):

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

的 `SHAPE` 和 `COORDS` 属性 `AREA` 可在 `req=map` 请求，则 `AREA` 元素未经修改即可传递。 在大多数情况下，这涉及更改 `SHAPE` 值 `DEFAULT` to `RECT` (这也会将 `COORDS` 属性)，或更改 `COORDS` 值。

任意 `AREA` 在处理期间变为空的元素将被完全删除。 如果地图与 `layer=comp` 它被放在所有其他地图的后面。 数据以文本形式一返回为一个或多个HTML `AREA` 元素。 空的回复字符串表示指定对象不存在图像映射。

地图处理不考虑图层透明度。 完全透明的图层仍然可以与其关联图像映射。 部分透明层的映射不会被剪切到透明区域。

## 另请参阅 {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [目录：:Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML4.01规范](https://www.w3.org/TR/html401/)
