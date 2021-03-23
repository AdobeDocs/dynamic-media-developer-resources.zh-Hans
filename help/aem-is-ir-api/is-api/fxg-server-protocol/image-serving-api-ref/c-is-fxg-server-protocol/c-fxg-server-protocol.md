---
description: 要处理图形，您可以使用参考点（类似于罗经点）。
seo-description: 要处理图形，您可以使用参考点（类似于罗经点）。
seo-title: FXG服务器协议
solution: Experience Manager
title: FXG服务器协议
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 83%

---


# FXG服务器协议{#fxg-server-protocol}

要处理图形，您可以使用参考点（类似于罗经点）。

使用参考点，您可以相对于某个特定参考点旋转、缩放或调整图形的大小。参考点为`northWest`、`north`、`northEast`、`west`、`center`、`east`、`southWest`、`south`和`southeast`。 例如，通过使用 center 参考点，您可以将一个图形绕其中心旋转 45 度。下图显示了参考点的位置、一个图形、该图形从其 `northWest` 参考点旋转 20 度所得到的图形和从其 `east` 参考点旋转 20 度所得到的图形。

![](assets/wp_ref_points.png)

* A.参考点位置
* B.图
* C.图形从其`northWest`参考点旋转了20度
* D.图形从其`east`参考点旋转了20度

语法如下：

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

默认值为 none。`inherit` 值将 `s7:referencePoint` 值从页面顶部或组级别传递到所有子项，但前提是它未设置为 `none`。`none` 设置表示该对象没有参考点，使用 FXG 坐标系。

>[!NOTE]
>
>要使用参考点，并且该对象在处理之后不包含任何置换，请在处理新该对象之后更新它的 x 和 y 值。

当`s7:referencePoint` 的值与组（或路径、线元素或任何没有明确定义宽度和高度的元素）一起使用时，该值将应用于该组的累积定界框。例如，该组中所有对象的定界框左上方的点用作该组的 `northWest` 参考点；右下方的点用作 `southEast` 参考点。

