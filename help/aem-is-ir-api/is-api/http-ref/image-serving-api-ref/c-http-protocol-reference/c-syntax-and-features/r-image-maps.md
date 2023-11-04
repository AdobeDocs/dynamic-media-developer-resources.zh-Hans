---
description: IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 图像映射{#image-maps}

IS提供了简化HTML图像映射使用的机制。 IS中基于JAVA和基于Flash的查看器还包括对图像映射的有限支持。

通过以下任一方式将源图像映射提供给IS `catalog::Map` 或使用 `map=` 命令和已处理的映射使用 `req=map` 命令。

图像映射由一个或多个HTMLAREA元素组成，使用“&lt;”和“>”正确分隔。 如果通过catalog：：Map提供，则假定所有像素坐标值均采用原始图像分辨率，并相对于（未修改的）源图像的左上角。 当通过 `map=` 命令，假定坐标值是图层坐标，相对于图层的左上角(在 `rotate=` 和 `extend=`)。

>[!NOTE]
>
>此时不允许使用%坐标，处理方式可能不正确。

IS通过将空间变换（例如缩放和旋转）应用于地图坐标，然后以适当的z顺序（从前到后）和适当的位置组装处理过的图层地图，从每个组成层的源图像地图生成合成图像地图。

与一起提供时，将考虑使用以下命令进行图像映射处理 `req=map` (直接在请求中，通过目录模板，或在 `catalog::Modifier` 字符串)：

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

所有其他命令将被有效忽略。

此 `SHAPE` 和 `COORDS` 属性 `AREA` 在处理期间可以修改 `req=map` 请求，的所有其他属性 `AREA` 元素无需修改即可传递。 在大多数情况下，这涉及到更改 `SHAPE` 值自 `DEFAULT` 到 `RECT` (这也会添加 `COORDS` 属性)，或更改 `COORDS` 值。

任何 `AREA` 处理期间变为空的元素将被完全删除。 如果映射与 `layer=comp` 它位于所有其他地图之后。 数据以文本形式作为或多个HTML返回 `AREA` 元素。 空回复字符串表示指定对象不存在图像映射。

处理映射时不考虑图层透明度。 完全透明的图层仍然可以具有与其关联的图像映射。 部分透明层的映射不会裁剪到透明区域。

## 另请参阅 {#see-also}

[映射=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ， [catalog：：Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)， [HTML4.01规范](https://www.w3.org/TR/html401/)
