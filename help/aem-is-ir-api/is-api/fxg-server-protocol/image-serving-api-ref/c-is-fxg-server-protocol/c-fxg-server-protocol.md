---
title: FXG服务器协议
description: 要处理图形，您可以使用参考点（类似于罗经点）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# FXG服务器协议{#fxg-server-protocol}

要处理图形，您可以使用参考点（类似于罗经点）。

使用参考点，您可以相对于某个特定参考点旋转、缩放或调整图形的大小。 参考点为`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`和`southeast`。 例如，通过使用中心参照点，可以将图形中心旋转45°。 下图显示了参考点所在的位置、图形、图形从其`northWest`参考点旋转20°，以及图形从其`east`参考点旋转20°。

![参考点图像](assets/wp_ref_points.png)

* A.参考点位置
* B. 图形
* C.图形从其`northWest`参考点旋转20°
* D.图形从其`east`参考点旋转20°

语法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

默认值为none。 `inherit`值将`s7:referencePoint`值（如果它不是`none`）从页面或组级别的顶部传递到所有子级。 `none`设置意味着对象没有参考点，并且使用了FXG坐标系。

>[!NOTE]
>
>要使用参考点，并且该对象在处理之后不包含任何置换，请在处理新该对象之后更新它的 x 和 y 值。

当来自`s7:referencePoint`的值用于组（或路径、行元素或没有显式宽度和高度定义的任何元素）时，该值应用于组的累积定界框。 例如，组中所有对象边界框的左上角用作组的`northWest`参考点；右下角用作`southEast`参考点。
